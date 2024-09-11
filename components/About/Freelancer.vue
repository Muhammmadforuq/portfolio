<script setup>
  const aboutme = [
    // 1
    {
      id:1,
      title: 'Fullname : ',
      text: 'Bekzodbek Sobirov',
    },
    // 2
    {
      id:2,
      title: 'Email : ',
      text: 'alforuq0003@gmail.com',
     },
   
    // 3
    {
      id:3,
      title: 'Nationality : ',
      text: 'Uzbekistan',
    },
    // 
    {
      id:4,
      title: 'Phone : ',
      text: '+998 93 417 08 17',
    },
    // 5
    {
      id:5,
      title: 'Age : ',
      text: '21',
    },
       {
      id:6,
      title: 'Languages : ',
      text: 'Uzbek, English',
    },

       {
      id:7,
      title: 'Experience : ',
      text: '2+ years',
    },
     {
      id:8,
      title: 'Freelance : ',
      text: 'Available',
    },


  ]
</script>
<template>
  <div class="space-y-4">
    <h2 class="text-3xl font-bold">Frontend Developer</h2>
    <p class="max-w-xl min-h-24 text-white/80 mt-3">
      Frontend developer with experience in 20+ projects, skilled in HTML, CSS, Tailwind, JavaScript, Vue.js, and Nuxt.js, creating dynamic and responsive web apps.
    </p>
    <div class="grid grid-cols-2 gap-4">
        <div v-for="item in aboutme" :key="item.id" class="flex items-center gap-2">
          <h3 class="font-medium text-lg">{{ item.title }}</h3>
          <p class="text-neutral-300">{{ item.text }}</p>
        </div>
    </div>
  </div>
</template>

