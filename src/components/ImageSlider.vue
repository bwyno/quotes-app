<template>
  <div class="grid grid-cols-8">
    <div ref="firstImg" class="none hover:h-[500px]" v-for="index in 16" :key="index">
      <img :src="`/solo-${index}.svg`" height="500" />
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const firstImg = ref()
</script>