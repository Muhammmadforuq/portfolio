<script setup>

import 'primeicons/primeicons.css';
const router = useRouter();

const socialLinks = [
  {
    icon: 'pi pi-github',
    link: 'https://github.com/mforuq',
  },
  {
    icon: 'pi pi-linkedin',
    link: 'https://www.linkedin.com/in/mforuq',
  },
  {
    icon: 'pi pi-youtube',
    link: 'https://www.youtube.com/mforuq',
  },


  {
    icon: 'pi pi-envelope',
    link: 'mailto:mforuq@gmail.com',
  },
  {
    icon: 'pi pi-phone',
    link: 'tel:+6285777777777',
  },

];
</script>
<template>
  <header class="absolute top-0 left-0 w-full z-30">
    <nav class="container mx-auto flex justify-between items-center py-4">
      <NuxtLink to="/" class="text-2xl font-bold text-white"><span class="text-accent">M</span>Foruq</NuxtLink>
      <div class="flex items-center gap-4">
        <NuxtLink v-for="link in socialLinks" :key="link.link" :to="link.link" target="_blank" class="text-white hover:text-accent transition-all">
            <i :class="link.icon" class="text-lg"></i>
        </NuxtLink>
      </div>
    </nav>
  </header>
</template>


