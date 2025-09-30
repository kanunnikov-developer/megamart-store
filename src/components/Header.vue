<script setup>
import { ref, inject } from "vue";
import Line from "../share/Line.vue";

const search = ref("");
const { cart } = inject("cart");

function getSearch(text) {
  console.log(search.value);
}
</script>

<template>
  <header>
    <div class="container">
      <div class="header">
        <a href="/"
          ><img src="../icons/MegaMart.svg" alt="MegaMart" class="logo"
        /></a>
        <div class="block-input">
          <img src="../icons/Search.svg" alt="Search" class="searchIcon" />
          <input
            type="text"
            placeholder="Search essentials, groceries and more..."
            v-model="search"
            @keyup.enter="getSearch(search)"
          />
        </div>
        <div class="profile">
          <button class="profile-button">
            <img src="../icons/user.svg" alt="User" class="img-profile" />
            Sign Up/Sign In
          </button>
          <Line />
          <button class="profile-button">
            <div class="cart-icon-container">
              <img src="../icons/Buy.svg" alt="Cart" class="img-profile" />
              <span v-if="cart.length > 0" class="cart-counter">{{
                cart.length
              }}</span>
            </div>
            <p>Cart</p>
          </button>
        </div>
      </div>
    </div>
  </header>
</template>

<style scoped>
.header {
  padding: 20px 0px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.block-input {
  width: 500px;
  padding: 15px;
  display: flex;
  align-items: center;
  gap: 10px;
  background: var(--bg-3-color);
  border-radius: 10px;
}

.logo {
  width: 138px;
  height: 28px;
}

.searchIcon {
  width: 18px;
  height: 18px;
}

.img-profile {
  width: 24px;
  height: 24px;
}

input {
  border: none;
  width: 100%;
}

input::placeholder {
  opacity: 50%;
}

.profile {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 10px;
}

.profile-button {
  display: flex;
  align-items: center;
  gap: 6px;
}

button {
  padding: 12px 15px;
  border-radius: 10px;
  font-weight: 600;
  transition: all 0.1s ease-in;
}

button:hover {
  background: var(--bg-3-color);
  transition: all 0.1s ease-in;
}

.cart-icon-container {
  position: relative;
  display: inline-block;
}

.cart-counter {
  position: absolute;
  top: -8px;
  right: -8px;
  background: #ff4444;
  color: white;
  border-radius: 50%;
  width: 20px;
  height: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 12px;
  font-weight: bold;
  min-width: 20px;
  line-height: 1;
}
</style>
