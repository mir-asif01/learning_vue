<script setup>
import Navbar from "./components/Navbar.vue"
import Hero from "./components/Hero.vue"
import HomeCards from "./components/HomeCards.vue"
</script>

<template>
  <Navbar />
  <Hero title="title from prop" description="description from props" />
  <HomeCards />
</template>
