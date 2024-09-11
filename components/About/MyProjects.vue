<script setup>
  const projects = [
    {
      data: 'Jun 2023',
      name: 'Campus Multimedia',
      tools: ['Html,', 'Tailwindcss,', 'JavaScript'],
    },
    {
      data: 'Feb 2024',
      name: 'Ai-short',
      tools: ['Tailwindcss,', 'Vue,js'],
    },
    {
      data: 'Jun 2024',
      name: 'Relook',
      tools: ['Html,', 'Tailwindcss,', 'Nuxt.js,', "Swiper.js"],
    },
    {
      data: 'Jun 2024',
      name: 'Eagerwork',
      tools: ['Html,', 'Tailwindcss,', 'JavaScript,'],
    },
  ]
</script>
<template>
  <div class="space-y-4">
    <h2 class="text-3xl font-bold">My Projects</h2>
    <p class="max-w-xl min-h-24">
      Over 20 frontend projects completed, delivering engaging and dynamic web experiences using Vue.js, Nuxt.js, Tailwind CSS, and JavaScript.
    </p>
    <div class="grid grid-cols-2 gap-4">
      <div v-for="project in projects" :key="project.name" class="bg-neutral-700 rounded-xl px-5 py-6">
        <h4 class="font-medium text-orange-500">{{ project.data }}</h4>
        <h3 class="font-mono text-xl/6 font-semibold min-h-8 mt-3">{{ project.name }}</h3>
        <div class="flex items-center text-sm gap-2 mt-4">
          <span class="size-4 rounded-full bg-orange-500"></span>
          <p v-for="tool in project.tools" :key="tool" class="text-neutral-300 text-sm">{{ tool }}</p>
        </div>
      </div>

   
    </div>
  </div>
</template>


