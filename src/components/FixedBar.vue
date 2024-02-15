<template>
  <div class="fixed-bottom-bar relative flex justify-center items-center">
    <div class="text-white absolute z-[2]">Scroll down as we chase memories, one adventure at a time.</div>
    <div class="scroll-watcher w-full h-full z-[1] top-0"></div>
  </div>
</template>
<style>
.fixed-bottom-bar {
  position: fixed;
  width: 100%;
  bottom: 0;
  height: 30px;
  background-color:#B7410E ;
  
}

.scroll-watcher {
  background-color:#5A2D83  ;
  scale: 0.5 1;
  transform-origin: left;
  animation: scroll-watcher linear;
  animation-timeline: scroll();
} 

@keyframes scroll-watcher {
  to { scale: 0 1; }
}
</style>