<script setup>
import ZeroHero from "./components/ZeroHero.vue";
import Header from "./components/Header.vue";
import Hero from "./components/Hero.vue";
import Products from "./components/Products.vue";
import { provide, ref } from "vue";
import Categories from "./components/Categories.vue";

let cart = ref([]);

function addToCart(product) {
  cart.value.push(product);
}

provide("cart", {
  cart,
  addToCart,
});
</script>

<template>
  <ZeroHero />
  <Header />
  <div class="border"></div>
  <Hero />
  <Products />
  <Categories />
</template>

<style scoped>
.border {
  width: 100%;
  height: 1px;
  background: var(--border);
}
</style>
