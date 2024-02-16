<template>
  <section class="section-two flex justify-center items-center h-screen px-[60px]">
    <div class="grid grid-cols-1 items-center gap-10 md:grid-cols-2 md:gap-0">
      <div class="flex items-center justify-center">
        <div class="text-[20px] text-center md:text-justify md:w-[800px]">
          Every day brings forth a new treasure, my dear Nica, from this collection of 100 heartfelt
          messages. Whether a poignant quote or a lyrical verse, each one stands as a testament to
          my enduring love for you.
        </div>
      </div>
      <div class="grid grid-cols-1 text-center gap-5">
        <div class="text-[60px] md:text-[70px]">{{ dat.id }}</div>
        <div class="text-base md:text-[40px]">{{ todayDate }}</div>
        <div class="text-[20px] md:text-[30px]">{{ dat.message }}</div>
      </div>
    </div>
  </section>
</template>
<script setup lang="ts">
interface DataItem {
  id: number
  date: string
  message: string
}

import { ref, onMounted } from 'vue'
import data from '@/assets/csvjson.json'
const todayDate = ref(
  new Date().toLocaleDateString('en-US', {
    month: 'long',
    day: 'numeric',
    year: 'numeric'
  })
)

const dat = ref<DataItem>({ id: 0, date: '', message: '' })

onMounted(() => {
  let foundMatch = false
  for (const item of data) {
    if (item.date === todayDate.value.toString()) {
      dat.value = item
      foundMatch = true
      break // Break out of the loop once a match is found
    }
  }
  if (!foundMatch) {
    dat.value = data[Math.floor(Math.random() * 100)] // Use 100 instead of 101
  }

  console.log(dat.value)
})
</script>
<style>
.section-two {
  width: auto;
  flex-shrink: 0;
  overflow: hidden;
  animation: fade-in linear forwards;
  animation-timeline: view();
  animation-range: entry;
}
</style>
