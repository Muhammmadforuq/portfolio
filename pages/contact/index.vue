<template>
    <div class="relative bg-primary/60 h-full">
      <div class="relative max-w-2xl mx-auto pt-44 pb-10 z-20">
        <h1 class="text-5xl font-bold text-center">Let's work together</h1>
        <form @submit.prevent="sumbitMessage" class="grid grid-cols-2 gap-4 mt-8">
          <input v-model="client.name" type="text" required placeholder="Name" class="bg-white/10 border border-white/20 focus:outline-none rounded-md p-2" />
          <input v-model="client.email" type="email" required placeholder="Email" class="bg-white/10 border border-white/20 focus:outline-none rounded-md p-2" />
          <input v-model="client.subject" type="text" required placeholder="Subject" class="col-span-2 bg-white/10 border border-white/20 focus:outline-none rounded-md p-2" />
          <textarea v-model="client.message" required placeholder="Message" class="col-span-2 h-32 resize-none bg-white/10 border border-white/20 focus:outline-none rounded-md p-2"></textarea>
          <div>
            <button type="submit" class="bg-orange-500 text-white rounded-md py-2 px-10">Send</button>
          </div>
        </form>
      </div>
      <div class="absolute bottom-0 left-0 w-full h-full bg-gradient-to-bl from-orange-700/50 to-primary/50"></div>
  </div>
</template>

<script setup>
const client = ref(
    {
    name: '',
    email: '',
    subject: '',
    message: ''
  }
)


const sumbitMessage = () => {
  console.log(client.value);
  client.value.name = '';
  client.value.email = '';
  client.value.subject = '';
  client.value.message = '';
}
</script>