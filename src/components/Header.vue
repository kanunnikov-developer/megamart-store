<script setup>
import Line from "../share/Line.vue";
import Button from "../share/Button.vue";
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
          />
        </div>
        <div class="profile">
          <button class="profile-button">
            <img src="../icons/user.svg" alt="User" class="img-profile" />
            Sign Up/Sign In
          </button>
          <Line />
          <button class="profile-button">
            <img src="../icons/Buy.svg" alt="Cart" class="img-profile" />
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
</style>
