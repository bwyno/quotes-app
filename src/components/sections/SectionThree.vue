<template>
  <section
    id="nica"
    class="section-three flex flex-col gap-[80px] h-screen justify-center items-center"
  >
    <div class="text-center w-4/5 text-[40px]">
      <i>
        "Through the years, you've blossomed into an extraordinary woman, radiating strength, grace,
        and compassion. You deserve nothing less than the universe itself."
      </i>
    </div>
    <div class="flex flex-row">
      <img
        v-for="index in 8"
        :key="index"
        class="set-1 shrink-0 h-[300px] w-[300px]"
        :src="`/solo-${index}.svg`"
        height="300"
      />
    </div>
    <div class="flex flex-row">
      <img
        v-for="index in 8"
        :key="index"
        class="set-2 shrink-0 h-[300px] w-[300px]"
        :src="`/solo-${index + 8}.svg`"
        height="300"
      />
    </div>
  </section>
</template>
<script setup lang="ts"></script>
<style>
.section-three {
  width: auto;
  /* height: auto; */
  flex-shrink: 0;
  overflow: hidden;
  animation: fade-in linear forwards;
  animation-timeline: view();
  animation-range: entry;
}

@keyframes fade-in {
  from {
    scale: 0.8;
    opacity: 0;
  }
  to {
    scale: 1;
    opacity: 1;
  }
}

.set-1 {
  animation: scrolling linear;
  animation-timeline: scroll(root);
}

@keyframes scrolling {
  from {
    transform: translateX(-500%);
  }
  to {
    transform: translateX(400%);
  }
}

.set-2 {
  animation: scrolling-2 linear;
  animation-timeline: scroll(root);
}

@keyframes scrolling-2 {
  from {
    transform: translateX(500%);
  }
  to {
    transform: translateX(-400%);
  }
}
</style>
