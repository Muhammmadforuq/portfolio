<script setup>
const services = [
  {
    id: 1,
    links:[
      {
        id:1,
        link:'Website',
        img:'thumb1',
      },
      {
        id:2,
        link:'Website',
        img:'thumb2',
      },
      {
        id:3,
        link:'Website',
        img:'thumb3',
      },
      {
        id:4,
        link:'Website',
        img:'thumb4',
      },

    ]
  },
  {
    id: 1,
    links:[
      {
        id:1,
        link:'Website',
        img:'thumb4',
      },
      {
        id:2,
        link:'Website',
        img:'thumb3',
      },
      {
        id:3,
        link:'Website',
        img:'thumb1',
      },
      {
        id:4,
        link:'Website',
        img:'thumb2',
      },

    ]
  },

 
]
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/pagination';
import { Pagination } from 'swiper/modules';
import { ArrowRightIcon} from '@heroicons/vue/24/solid';
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
            slidesPerView: 1,
            spaceBetween: 20,
          },
                }"
            >
              <SwiperSlide v-for="service in services" :key="service.id">
                <div class="grid grid-cols-2 gap-4">
                  <div v-for="link in service.links" :key="link.id" class="relative group cursor-pointer overflow-hidden h-52 rounded-lg">
                    <img :src="`/${link.img}.jpg`" class="absolute top-0 left-0 size-full object-cover">
                    <!-- live project -->
                    <div class="absolute top-0 left-0 size-full group-hover:bg-black/70 transition-all duration-300 bg-black/0"></div>
                    <div class="relative flex items-center justify-center gap-2 z-10 h-full">
                        <p class="absolute font-poppins font-medium leading-none -bottom-full group-hover:bottom-1/2 transition-all duration-300">Live Project</p>
                        <ArrowRightIcon class="size-4 stroke-[4px] absolute -bottom-full right-28 group-hover:bottom-1/2 transition-all duration-700"/>
                      </div>
                  </div>
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


