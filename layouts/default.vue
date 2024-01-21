<template>
  <div class="container mx-auto max-w-2xl">
    <header class="flex justify-between items-center mt-5">
      <div class="flex items-center space-x-12">
        <div>
        <nuxt-link to="/"
                   class="text-xl font-semibold p-2 hover:bg-gray-200">Alex Firulin</nuxt-link>
      </div>
      <the-menue />
      </div>
      <client-only>
        <the-color-mode-celector></the-color-mode-celector>
      </client-only>

    </header>
    <main class="mt-10">
      <slot />
    </main>
  </div>
</template>

<script setup>
useHead({
  titleTempalte: '%s - Alex Firulin'
})
link: [
  {
    rel:'preconnect',
    href: 'https://fonts.googleapis.com/'
  },
  {
     href: "https://fonts.googleapis.com/css2?family=Instrument+Sans&family=Roboto:ital@1&display=swap",
     rel: "stylesheet",
     crossorigin: ''
  }
]
</script>

<style>
body{
font-family: 'Roboto';
}

body {
  @apply bg-white dark:bg-gray-900 text-gray-700 dark:text-gray-300
}
</style>
