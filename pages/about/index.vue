<script setup>
  const tabs = ref([
    {
      id:1,
      name:'About Me',
    },
    {
      id:2,
      name:'Education',
    },
    {
      id:3,
      name:'My Projects',
    },
    {
      id:4,
      name:'Skills',
    },
    
  ])
  const activeTab = ref(1);

  const handleTabClick = (tab) => {
    activeTab.value = tab;
  } 
</script>

<template>
  <div class="relative bg-primary/60 h-full">
    <div class="relative container mx-auto pt-44 pb-10 z-20">
      <div class="grid md:grid-cols-3 gap-8">
        <div class="space-y-5">
          <h1 class="text-5xl font-bold">Why hire me?</h1>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus tenetur velit
          </p>
          <div class="font-medium font-mono space-y-4">
            <button type="button" v-for="(tab, index) in tabs" :key="index" :class="tab.id === activeTab ? 'bg-orange-500' : 'bg-neutral-700'" class="w-full hover:bg-orange-500 transition-colors duration-300 rounded px-8 py-2" @click="handleTabClick(tab.id)">
              {{ tab.name }}
            </button>
          </div>
        </div>
        <div class="col-span-2">
          <AboutFreelancer v-if="activeTab == 1" />
          <AboutEducation v-if="activeTab == 2"/>
          <AboutMyProjects v-if="activeTab == 3"/>
          <AboutSkills v-if="activeTab == 4"/>
        </div>
      </div>
    </div>
    <div class="absolute bottom-0 left-0 w-full h-full bg-gradient-to-bl from-orange-700/50 to-primary/50"></div>
  </div>
</template>

