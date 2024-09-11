<!-- <script setup>
import { useMotion } from '@vueuse/motion';

// Define motion settings
const motionSettings = {
  initial: { x: 100, width: '100%' },
  enter: { x: 0, width: '100%', transition: { duration: 1, delay: 0.5 } },
  leave: { x: 100, width: '0%', transition: { duration: 1.5, delay: 0.2 } }
};
</script> -->

<!-- <template>
  <div class="h-full" v-motion="motionSettings">
    <div class="fixed top-0 h-screen right-full w-screen bg-[#2e2257] z-30">
      <slot />
    </div>
  </div>
  
  <div class="h-full" v-motion="{ initial: { x: 100, width: '100%' }, enter: { x: 0, width: '100%' }, leave: { x: 100, width: '0%' }, transition: { delay: 0.4, duration: 0.6, ease: 'easeInOut' } }">
    <div class="fixed top-0 h-screen right-full w-screen bg-[#3b2d] z-20">
      <slot />
    </div>
  </div>
  
  <div class="h-full" v-motion="{ initial: { x: 100, width: '100%' }, enter: { x: 0, width: '100%' }, leave: { x: 100, width: '0%' }, transition: { delay: 0.2, duration: 0.6, ease: 'easeInOut' } }">
    <div class="fixed top-0 h-screen right-full w-screen bg-[#2e2257] z-20">
      <slot />
    </div>
  </div>
</template> -->
<template>
  <div>
    <slot />
  </div>
</template>
