<script setup>
import ZeroHero from "./components/ZeroHero.vue";
import Header from "./components/Header.vue";
import Hero from "./components/Hero.vue";
import ProductsList from "./components/ProductsList.vue";
import CategoriesList from "./components/CategoriesList.vue";
import { provide, ref } from "vue";
import TitleBlock from "./components/TitleBlock.vue";

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
  <TitleBlock title="Grab the best deal on" accent-text="Smartphones"
    ><ProductsList
  /></TitleBlock>
  <TitleBlock title="Shop From" accent-text="Top Categories"
    ><CategoriesList
  /></TitleBlock>
</template>

<style scoped>
.border {
  width: 100%;
  height: 1px;
  background: var(--border);
}
</style>
