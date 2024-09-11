<template>
  <div ref="container" class="transition-container size-full flex justify-center items-center">
    <!-- Define 4 columns -->
    <div ref="columns" class="grid grid-cols-4 size-full">
      <div class="column h-full bg-blue-500"></div>
      <div class="column h-full bg-green-500"></div>
      <div class="column h-full bg-red-500"></div>
      <div class="column h-full bg-yellow-500"></div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount } from "vue";
import { gsap } from "gsap";

// Refs for the container and columns
const container = ref(null);
const columns = ref(null);

// Function to animate the container and columns
const animateIn = () => {
  gsap.from(container.value, {
    duration: 1,
    opacity: 0,
    ease: "power3.out",
  });

  gsap.fromTo(
    columns.value.children,
    {
      opacity: 0,
      y: 100, // Start position below
    },
    {
      opacity: 1,
      y: 0, // End position at the original spot
      ease: "power3.out",
      duration: 1,
      stagger: 0.5, // Delay between animations for a sequential effect
    }
  );
};

// Function to reset animation for exit
const animateOut = () => {
  gsap.to(container.value, {
    duration: 0.5,
    opacity: 0,
    ease: "power3.in",
    onComplete: () => {
      container.value.style.display = 'none'; // Hide element after animation
    }
  });

  gsap.to(columns.value.children, {
    opacity: 0,
    y: -100, // Move columns up
    ease: "power3.in",
    duration: 0.5,
    stagger: 0.3,
  });
};

// Trigger animation on mounted
onMounted(() => {
  animateIn();
});

// Handle component cleanup and exit animation
onBeforeUnmount(() => {
  animateOut();
});
</script>

<style scoped>
.transition-container {
  @apply w-full h-full;
}
.column {
  @apply h-full rounded-lg;
}
</style>
