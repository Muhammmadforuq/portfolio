<script setup>
import HtmlIcon from '@/components/icon/HtmlIcon.vue';
import CssIcon from '@/components/icon/CssIcon.vue';
import JavaScriptIcon from '@/components/icon/JavaScriptIcon.vue';
import TailwindIcon from '@/components/icon/TailwindIcon.vue';
import FigmaIcon from '@/components/icon/FigmaIcon.vue';
import VueLogo from '@/components/icon/VueLogo.vue';
import NuxtIcon from '@/components/icon/NuxtIcon.vue';
import PiniaIcon from '@/components/icon/PIniaIcon.vue';

const skills = [
  {
    id: 1,
    name: 'HTML',
    icon: HtmlIcon,
  },
  {
    id: 2,
    name: 'CSS',
    icon: CssIcon,
  },
  {
    id: 3,
    name: 'Tailwindcss',
    icon: TailwindIcon,
  },
  {
    id: 4,
    name: 'JavaScript',
    icon: JavaScriptIcon,
  },
  {
    id: 5,
    name: 'Vue.js',
    icon: VueLogo,
  },
  {
    id: 6,
    name: 'Nuxt.js',
    icon: NuxtIcon,
  },
  {
    id: 7,
    name: 'Pinia',
    icon: PiniaIcon,
  },
  {
    id: 8,
    name: 'Figma',
    icon: FigmaIcon,
  },

  
];
</script>

<template>
  <div class="space-y-4">
    <h2 class="text-3xl font-bold">Skills</h2>
    <p class="max-w-xl min-h-24">
      Over 20 frontend projects completed, delivering engaging and dynamic web experiences using Vue.js, Nuxt.js, Tailwind CSS, and JavaScript.
    </p>
    <div class="grid grid-cols-4 gap-4">
      <div v-for="skill in skills" :key="skill.id" class="relative h-32 cursor-pointer bg-neutral-700 rounded-md px-5 py-6 flex items-center justify-center overflow-hidden">
        <!-- Dynamically render the icon component -->
        <component :is="skill.icon" class="size-16" />
        <!-- tool tip -->
        <div class="absolute top-0 left-0 w-full h-full bg-black/50 opacity-0 hover:opacity-100 transition-opacity duration-300 flex items-center justify-center">
          <p class="font-medium text-white text-center">{{ skill.name }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
