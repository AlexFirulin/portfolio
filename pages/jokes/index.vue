<template>
  <div class="flex flex-col justify-evenly items-center">
 <div>{{ data.joke }}</div>
</div>
</template>

<script setup>

const { data } = await useAsyncData(() => $fetch('https://geek-jokes.sameerkumar.website/api?format=json'))
</script>
