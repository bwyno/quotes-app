<template>
  <section class="section-four justify-center flex items-center h-screen flex-col">
    <div class="grid grid-cols-2 w-4/5">
      <div class="text-[40px] z-20 flex h-screen justify-center items-center">
        I'm so thankful that you came into my life. Words can't express how happy I am to have you,
        my love.
      </div>
      <div class="flex justify-center items-center">
        <div class="h-[600px] flex flex-col gap-[100px] overflow-hidden items-center">
          <img
            v-for="index in 23"
            :key="index"
            class="set-3 shrink-0 h-[500px]"
            :src="`/duo-${index}.svg`"
            height="300"
          />
          <img src="/sunflower.svg" class="absolute top-[30] left-[0]" alt="">
        </div>
      </div>
    </div>
  </section>
</template>
<script setup lang="ts"></script>

<style>
.section-four {
  width: auto;
  flex-shrink: 0;
  overflow: hidden;
  animation: fade-in linear forwards;
  animation-timeline: view();
  animation-range: entry;
}

.set-3 {
  animation: scrolling-3 linear 90s infinite;
}

@keyframes scrolling-3 {
  from {
    transform: translateY(100%);
  }
  to {
    transform: translateY(-2800%);
  }
}
</style>
