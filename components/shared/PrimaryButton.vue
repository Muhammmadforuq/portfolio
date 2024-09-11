<template>
  <NuxtLink :to="link" class="inline-block bg-orange-700 hover:bg-orange-800 text-white rounded-full transition-colors px-7 py-2">
    <slot />
  </NuxtLink>
</template>

<script setup>
  defineProps({
    link: {
      type: String,
      required: true,
    },
  });
</script>

