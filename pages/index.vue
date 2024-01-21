<template>
<div>
  Hello fron the main
</div>
</template>

<script setup>
useSeoMeta({
  title: 'Main page for my personal blog',
  description: '[Main page for my personal blog]',
  ogTitle: '[Main page for my personal blog]',
  ogDescription: '[og:description]',
  ogImage: '[og:image]',
  ogUrl: '[og:url]',
  twitterTitle: '[Main page for my personal blog]',
  twitterDescription: '[Main page for my personal blog]',
  twitterImage: '[twitter:image]',
  twitterCard: 'summary'
})

useHead({
  htmlAttrs: {
    lang: 'en'
  },
  link: [
    {
      rel: 'icon',
      type: 'image/png',
      href: '/favicon.png'
    }
  ]
})
</script>

<style>

</style>