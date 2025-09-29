<script setup>
import { ref } from "vue";
import Button from "../share/Button.vue";

const productsData = ref([
  {
    title: "Galaxy S22 Ultra",
    newPrice: "32 999",
    oldPrice: "74 999",
    img: "/img/Phone-1.svg",
  },
  {
    title: "Galaxy M13 (4GB | 64 GB )",
    newPrice: "10 499",
    oldPrice: "14999",
    img: "/img/Phone-2.svg",
  },
  {
    title: "Galaxy M33 (4GB | 64 GB )",
    newPrice: "16 999",
    oldPrice: "24 999",
    img: "/img/Phone-3.svg",
  },
  {
    title: "Galaxy M53 (4GB | 64 GB )",
    newPrice: "31 999",
    oldPrice: "40 999",
    img: "/img/Phone-4.svg",
  },
  {
    title: "Galaxy S22 Ultra",
    newPrice: "67 999",
    oldPrice: "85 999",
    img: "/img/Phone-5.svg",
  },
]);
</script>

<template>
  <div class="products-list">
    <div class="card" v-for="(product, index) in productsData" :key="index">
      <div class="phoneImg">
        <img :src="product.img" :alt="product.title" />
      </div>
      <div class="info">
        <h3 style="font-weight: 600">{{ product.title }}</h3>
        <div class="price">
          <p style="font-weight: 700">{{ product.newPrice }} ₽</p>
          <s v-if="product.oldPrice">{{ product.oldPrice }} ₽</s>
        </div>
        <div class="border"></div>
        <Button>Купить</Button>
      </div>
    </div>
  </div>
</template>

<style scoped>
.products-list {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 10px;
}

.card {
  border: 1px solid var(--border);
  border-radius: 16px;
}

.phoneImg {
  min-width: 224px;
  min-height: 188px;
  border-radius: 15px 15px 0 0;
  background: var(--bg-1-color);
  display: flex;
  align-items: center;
  justify-content: center;
}

.info {
  color: var(--text-black-color);
  padding: 12px;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.price {
  display: flex;
  align-items: center;
  gap: 13px;
}
</style>
