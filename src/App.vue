<script setup>
import ZeroHero from "./components/ZeroHero.vue";
import Header from "./components/Header.vue";
import Hero from "./components/Hero.vue";
import Products from "./components/Products.vue";
</script>

<template>
  <ZeroHero />
  <Header />
  <div class="border"></div>
  <Hero />
  <Products />
</template>

<style scoped>
.border {
  width: 100%;
  height: 1px;
  background: var(--border);
}
</style>
