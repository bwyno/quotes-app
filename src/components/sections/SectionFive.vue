<template>
  <section class="section-one justify-center flex items-center h-screen flex-col">
    <div class="text-[50px] text-center w-4/5">
      Happy Birthday my Love, May your day be filled with joy, laughter, and all the wonderful
      things life has to offer. Wishing you a fantastic year ahead!
    </div>
  </section>
</template>
<script setup lang="ts"></script>

<style>
.section-one {
  width: auto;
  flex-shrink: 0;
  overflow: hidden;
  animation: small-to-big linear forwards;
  animation-timeline: view();
  animation-range: entry;
}

@keyframes small-to-big {
  from {
    scale: 0.2;
  }
  to {
    scale: 1;
    opacity: 1;
  }
}
</style>
