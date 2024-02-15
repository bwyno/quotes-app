<template>
  <section class="section-two justify-center items-center grid grid-cols-2 h-screen px-[60px]">
    <div class="text-[30px] text-justify">
      Every day brings forth a new treasure, my dear Nica, from this collection of 100 heartfelt
      messages. Whether a poignant quote or a lyrical verse, each one stands as a testament to my
      enduring love for you.
    </div>
    <div class="grid-cols-1 text-center">
      <div class="text-[70px]">Countdown</div>
      <div class="text-[50px]">{{ todayDate }}</div>
      <div class="text-[120px]">Message</div>
    </div>
  </section>
</template>
<script setup lang="ts">
import { ref } from 'vue'
const todayDate = ref(
  new Date().toLocaleDateString('en-US', {
    month: 'long',
    day: 'numeric',
    year: 'numeric'
  })
)
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
