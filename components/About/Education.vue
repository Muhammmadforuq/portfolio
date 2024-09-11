<script setup>
  const Educations = [
    
    {
      data: '2021 - Current',
      name: 'Information technology',
      description: "Tashkent State Technical University",
    },
    {
      data: '2021',
      name: 'Common Front-end',
      description: "From his teachers",
    },
    {
      data: 'Jun 2024',
      name: 'JavaScript AkhrorWeb',
      description: "Online Course Platform",
    },
    {
      data: '2024',
      name: 'Vue.js, Nuxt.js, Pinia',
      description: "Fozilov Academy",
    },
  ]
</script>
<template>
  <div class="space-y-4">
    <h2 class="text-3xl font-bold">My Education</h2>
    <p class="max-w-xl min-h-24">
      Gained in-depth knowledge and practical experience in HTML, CSS, Tailwind CSS, JavaScript, Vue.js, and Nuxt.js through participation in 20+ frontend projects.
    </p>
    <div class="grid grid-cols-2 gap-4">
      <div v-for="education in Educations" :key="education.name" class="bg-neutral-700 rounded-xl px-5 py-6">
        <h4 class="font-medium text-orange-500">{{ education.data }}</h4>
        <h3 class="font-mono text-xl/6 font-semibold min-h-8 mt-3">{{ education.name }}</h3>
        <div class="flex items-center text-sm gap-2 mt-4">
          <span class="size-4 rounded-full bg-orange-500"></span>
          <p class="text-neutral-300 text-sm">{{ education.description }}</p>
        </div>
      </div>

   
    </div>
  </div>
</template>


