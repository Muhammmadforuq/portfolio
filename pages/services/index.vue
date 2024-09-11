<template>
  <div class="relative bg-primary/60 h-full">
    <div class="relative container mx-auto pt-48 pb-10 z-20">
      <div class="grid md:grid-cols-3 gap-8">
        <div class="space-y-5 mt-10">
          <h1 class="text-5xl font-bold">My Services</h1>
          <p>
            Transform your ideas into vibrant web experiences. With expertise in Vue.js, Nuxt.js, and Tailwind CSS, we build fast, engaging, and visually stunning websites that make an impact.
          </p>
          <SharedPrimaryButton :link="'/contact'">Contact Me</SharedPrimaryButton>
        </div>
        <div class="col-span-2">
          <ServicesSwiperCard />
        </div>
      </div>
    </div>
    <div class="absolute bottom-0 left-0 w-full h-full bg-gradient-to-bl from-orange-700/50 to-primary/50"></div>
  </div>
</template>
