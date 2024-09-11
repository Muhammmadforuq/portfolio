<script setup>
const services = [
  {
    id: 1,
    title: 'Custom Web Development',
    description: 'Tailored solutions for dynamic and responsive websites that meet your unique business needs.',
    icon:`<svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 24 24"><path fill="currentColor" d="m21 6.757l-2 2V4h-9v5H5v11h14v-2.757l2-2v5.765a.993.993 0 0 1-.993.992H3.993A1 1 0 0 1 3 20.993V8l6.003-6h10.995C20.55 2 21 2.455 21 2.992zm.778 2.05l1.414 1.415L15.414 18l-1.416-.002l.002-1.412z"/></svg>`,
  },
  {
    id: 2,
    title: 'Frontend Mastery',
    description: 'Expert development with Vue.js, Nuxt.js, and Tailwind CSS for seamless, interactive user experiences.',
    icon:`<svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 32 32"><path fill="currentColor" d="m23.6 21.4l3.6 3.6l-3.6 3.6L25 30l5-5l-5-5zm-3.2 0L16.8 25l3.6 3.6L19 30l-5-5l5-5z"/><path fill="currentColor" d="M28 8H16l-3.4-3.4c-.4-.4-.9-.6-1.4-.6H4c-1.1 0-2 .9-2 2v20c0 1.1.9 2 2 2h7v-2H4V6h7.2l3.4 3.4l.6.6H28v8h2v-8c0-1.1-.9-2-2-2"/></svg>`,
  },
  {
    id: 3,
    title: 'Performance Optimization',
    description: 'Enhancing speed, security, and scalability with modern frontend technologies and best practices.',
    icon:`<svg xmlns="http://www.w3.org/2000/svg" width="32" height="36" viewBox="0 0 14 14"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" d="m1.24 6.54l11.5-5.23M10.59.5l2.15.81l-.8 2.15m1.31 10.05h-2.5h0v-7a.5.5 0 0 1 .5-.5h1.5a.5.5 0 0 1 .5.5v7h0Zm-5 0h-2.5h0v-5.5a.5.5 0 0 1 .5-.5h1.5a.5.5 0 0 1 .5.5v5.5h0Zm-5 0H.75h0v-4a.5.5 0 0 1 .5-.5h1.5a.5.5 0 0 1 .5.5v4h0Z"/></svg>`,
  },
  {
    id: 4,
    title: 'UI/UX Design',
    description: "Creating visually appealing and user-friendly interfaces that engage and retain your audience.",
    icon:`<svg xmlns="http://www.w3.org/2000/svg" width="32" height="40" viewBox="0 0 384 512"><path fill="currentColor" d="M14 95.792C14 42.888 56.888 0 109.793 0h164.368c52.905 0 95.793 42.888 95.793 95.792c0 33.5-17.196 62.984-43.243 80.105c26.047 17.122 43.243 46.605 43.243 80.105c0 52.905-42.888 95.793-95.793 95.793h-2.08c-24.802 0-47.403-9.426-64.415-24.891v88.263c0 53.61-44.009 96.833-97.357 96.833C57.536 512 14 469.243 14 416.207c0-33.498 17.195-62.98 43.24-80.102C31.194 318.983 14 289.5 14 256.002c0-33.5 17.196-62.983 43.243-80.105C31.196 158.776 14 129.292 14 95.792m162.288 95.795h-66.495c-35.576 0-64.415 28.84-64.415 64.415c0 35.438 28.617 64.192 64.003 64.414l.412-.001h66.495zm31.378 64.415c0 35.575 28.839 64.415 64.415 64.415h2.08c35.576 0 64.415-28.84 64.415-64.415s-28.839-64.415-64.415-64.415h-2.08c-35.576 0-64.415 28.84-64.415 64.415m-97.873 95.793l-.412-.001c-35.386.221-64.003 28.975-64.003 64.413c0 35.445 29.225 64.415 64.931 64.415c36.282 0 65.979-29.436 65.979-65.455v-63.372zm0-320.417c-35.576 0-64.415 28.84-64.415 64.414c0 35.576 28.84 64.415 64.415 64.415h66.495V31.377zm97.873 128.829h66.495c35.576 0 64.415-28.839 64.415-64.415c0-35.575-28.839-64.414-64.415-64.414h-66.495z"/></svg>`
  },
 
]
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/pagination';
import { Pagination } from 'swiper/modules';
import { ArrowUpRightIcon} from '@heroicons/vue/24/solid';
</script>
<template>
  <Swiper 
    :modules="[Pagination]"
    :navigation="{ nextEl: '.product-next', prevEl: '.product-prev' }"
    :slides-per-view="1"
    :pagination="{ el: '.services-pagination', clickable: true }"
    :loop="false"
        :breakpoints="{
            375:{
                slidesPerView: 1,
                    spaceBetween: 20,
                },
          768: {
            slidesPerView: 2,
            spaceBetween: 20,
          },
          1024: {
            slidesPerView: 3,
            spaceBetween: 30,
          },
          1280: {
            slidesPerView: 3,
            spaceBetween: 30,
          },
          1536: {
            slidesPerView: 3,
            spaceBetween: 20,
          },
                }"
            >
              <SwiperSlide v-for="service in services" :key="service.id" class="group bg-neutral-700 hover:bg-neutral-600 transition-colors cursor-pointer rounded-xl px-5 py-6">
                <div>
                  <div v-html="service.icon" class="text-orange-500"></div>
                  <h3 class="min-h-14 text-lg font-bold mt-3">{{ service.title }}</h3>
                  <p class="font-poppins text-sm line-clamp-4 leading-6 mt-4">{{ service.description }}</p>
                  <ArrowUpRightIcon class="size-6 group-hover:rotate-45 transition-transform text-orange-500 mt-5" />
                </div>
              </SwiperSlide>
              
              <!-- Scrollbar -->
              <div class="services-pagination text-center space-x-5 mt-8"></div>
   </Swiper>
</template>
<style scoped>
  .services-pagination .swiper-pagination-bullet{
    @apply !size-6 shrink-0 !bg-white;
  }

  .services-pagination .swiper-pagination-bullet-active{
    @apply !bg-orange-500;
  }
</style>


