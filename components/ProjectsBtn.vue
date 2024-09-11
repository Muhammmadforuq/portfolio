<script setup>
  import { ArrowRightIcon } from '@heroicons/vue/24/solid';
</script>


<template>
   <NuxtLink to="/work" class="group flex justify-center items-center relative size-32 bg-circleStar bg-cover bg-no-repeat bg-center mt-6">
      <img src="/rounded-text.png" class="animate-spin-slow size-24 object-contain" alt="projects">
      <ArrowRightIcon class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 size-5 group-hover:scale-110 transition-transform duration-500" />
    </NuxtLink>
</template>

