<script setup>
import { ref } from "vue";

const productsData = ref([
  {
    title: "Mobile",
    img: "/img/categories/Mobile.svg",
  },
  {
    title: "Cosmetics",
    img: "/img/categories/Cosmetics.svg",
  },
  {
    title: "Electronics",
    img: "/img/categories/Electronics.svg",
  },
  {
    title: "Furniture",
    img: "/img/categories/Furniture.svg",
  },
  {
    title: "Watches",
    img: "/img/categories/Watches.svg",
  },
  {
    title: "Decor",
    img: "/img/categories/Decor.svg",
  },
  {
    title: "Accessories",
    img: "/img/categories/Accessories.svg",
  },
]);
</script>

<template>
  <div class="categories-list">
    <div
      class="categories"
      v-for="(category, index) in productsData"
      :key="index"
    >
      <div class="phoneImg">
        <img :src="category.img" :alt="category.title" />
      </div>
      <h3>{{ category.title }}</h3>
    </div>
  </div>
</template>

<style scoped>
.categories-list {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 10px;
}

.categories {
  cursor: pointer;
  padding: 25px 0px;
}

.phoneImg {
  min-width: 132px;
  min-height: 132px;
  border-radius: 100px;
  background: var(--bg-1-color);
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.1s ease-in;
  border: 1px solid var(--bg-1-color);
}

.phoneImg:hover {
  border: 1px solid var(--primary-color);
  transition: all 0.1s ease-in;
}

h3 {
  font-weight: 600;
  margin-top: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
