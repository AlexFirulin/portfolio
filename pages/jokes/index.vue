<template>
  <div class="flex flex-col justify-evenly items-center">
 <div>{{ data.joke }}</div>
 <button @click="fetchRandomJoke()" class="p-2 mt-8 max-w-40 border-gray-400 border">Random joke</button>
</div>
</template>

<script setup>
const { data } = await useAsyncData(() => $fetch('https://geek-jokes.sameerkumar.website/api?format=json')
)
const fetchRandomJoke = () => window.location.reload()
</script>
