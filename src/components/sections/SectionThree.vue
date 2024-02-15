<template>
  <section class="section-three flex flex-row gap-5 h-screen">
    <ImageSlider />
  </section>
</template>
<script setup lang="ts">
import ImageSlider from '../ImageSlider.vue'
</script>
<style>
.section-three {
  width: auto;
  /* height: auto; */
  flex-shrink: 0;
  overflow: hidden;
}
</style>
