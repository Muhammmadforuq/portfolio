<script setup>
  import { HomeIcon, RectangleGroupIcon, ViewColumnsIcon, EnvelopeIcon , UserIcon} from '@heroicons/vue/24/solid';

  const navData = [
    {
       name: 'home', path: '/', icon: HomeIcon,
    },
    { 
      name: 'about', path: '/about', icon:UserIcon  
    },
    { 
      name: 'services', path: '/services', icon:RectangleGroupIcon,
    },
    { 
      name: 'work', path: '/work', icon:ViewColumnsIcon
    },
    { 
      name: 'contact', path: '/contact', icon: EnvelopeIcon, 
    },
  ]
</script>

<template>
  <div class="fixed w-full lg:w-12 lg:max-w-md h-20 lg:h-max lg:right-[2%] z-50 bottom-0 lg:top-1/2 lg:-translate-y-1/2 flex flex-col justify-end lg:justify-between items-center gap-y-10">
    <div class="flex w-full lg:flex-col items-center justify-around lg:justify-center bg-white/10 backdrop-blur-sm
    gap-y-8 px-6 lg:px-0 py-5 rounded-full">
      <NuxtLink v-for="item in navData" :key="item.name" :to="item.path" class="group hover:scale-110 transition-transform" active-class="text-red-500">
        <div class="size-5 flex items-center justify-center">
          <component :is="item.icon" class="size-full text-current group-hover:text-accent transition-all duration-300" />
        </div>
        <!-- tooltip -->
        <div class="absolute right-0 top-1/2 -translate-y-1/2 hidden lg:group-hover:flex lg:items-center lg:justify-center pr-10">
          <div class="relative bg-white backdrop-blur-sm rounded-md px-3 py-1">
            <p class="font-medium text-xs text-primary">{{ item.name.charAt(0).toUpperCase() + item.name.slice(1) }}</p>
            <!-- triangle -->
            <div class="absolute -right-3 top-1/2 -translate-y-1/2 border-solid border-l-8 border-l-white border-y-transparent border-y-[6px] border-r-transparent border-r-[6px]"></div>
          </div>
        </div>
      </NuxtLink>
    </div>
  </div>
</template>
