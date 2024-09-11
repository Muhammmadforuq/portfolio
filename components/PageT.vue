<script setup>
import gsap from 'gsap';
// import { animationPageIn } from '@/utils/animation';
const animationPageIn = () => {
  const bannerOne = document.getElementById('banner-1');
  const bannerTwo = document.getElementById('banner-2');
  const bannerThree = document.getElementById('banner-3');
  const bannerFour = document.getElementById('banner-4');
  if (bannerOne && bannerTwo && bannerThree && bannerFour) {
    const tl = gsap.timeline();
    tl.set([bannerOne, bannerTwo, bannerThree, bannerFour], {
      yPercent: 0,
    }).to([bannerOne, bannerTwo, bannerThree, bannerFour], {
      yPercent: 100,
      stagger: 0.2,
      duration: 0.5,
      ease: 'power2.inOut'
    });
  }
}

const animationPageOut = (href) => {
  const bannerOne = document.getElementById('banner-1');
  const bannerTwo = document.getElementById('banner-2');
  const bannerThree = document.getElementById('banner-3');
  const bannerFour = document.getElementById('banner-4');
  if (bannerOne && bannerTwo && bannerThree && bannerFour) {
    const tl = gsap.timeline();
    tl.set([bannerOne, bannerTwo, bannerThree, bannerFour], {
      yPercent: -100,
    }).to([bannerOne, bannerTwo, bannerThree, bannerFour], {
      yPercent: 0,
      stagger: 0.2,
      duration: 0.5,
      ease: 'power2.inOut',
      onComplete: () => {
        router.push(href);
        // window.location.href = '/';
      }
    });
  }
}

onMounted(() => {
  animationPageIn();
});
</script>

<template>
  <div id="banner-1" class="min-h-screen fixed top-0 left-0 w-1/4 bg-neutral-950 z-10"></div>
  <div id="banner-2" class="min-h-screen fixed top-0 left-1/4 w-1/4 bg-neutral-950 z-10"></div>
  <div id="banner-3" class="min-h-screen fixed top-0 left-2/4 w-1/4 bg-neutral-950 z-10"></div>
  <div id="banner-4" class="min-h-screen fixed top-0 left-3/4 w-1/4 bg-neutral-950 z-10"></div>
</template>

