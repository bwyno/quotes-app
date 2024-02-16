<template>
  <div class="fixed-bottom-bar relative flex justify-center items-center h-[50px] md:h-[30px]">
    <div class="text-xs md:text-base text-white absolute z-[2]">Scroll down as we chase memories, one adventure at a time.</div>
    <div class="scroll-watcher w-full h-full z-[1] top-0"></div>
  </div>
</template>
<style>
.fixed-bottom-bar {
  position: fixed;
  width: 100%;
  bottom: 0;
  background-color:#B7410E ;
  
}

.scroll-watcher {
  background-color:#5A2D83  ;
  scale: 1 1;
  transform-origin: left;
  animation: scroll-watcher linear;
  animation-timeline: scroll();
} 

@keyframes scroll-watcher {
  to { scale: 0 1; }
}
</style>