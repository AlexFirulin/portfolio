<template>
  <NuxtLayout>
    <section>
      <h1 class="text-4xl mb-4"> Oops {{ error.statusCode }}</h1>
      <h2 class="text-xl text-gray-500 dark:"> {{ error.statusMessage }}</h2>
    </section>
  </NuxtLayout>
</template>

<script setup>
defineProps({error: Object})
</script>