<script setup>
import Line from "../share/Line.vue";
</script>

<template>
  <div class="zeroHero">
    <div class="container">
      <div class="block">
        <p>Welcome to worldwide Megamart!</p>
        <div class="info-list">
          <div class="info">
            <img src="../icons/Location.svg" alt="Location" />
            <p>Deliver to <span>423651</span></p>
          </div>
          <Line height="15" />
          <div class="info">
            <img src="../icons/Delivery.svg" alt="Delivery" />
            <p>Track your order</p>
          </div>
          <Line height="15" />
          <div class="info">
            <img src="../icons/Discount.svg" alt="Discount" />
            <p>All Offers</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.zeroHero {
  padding: 12px 0px;
  background: var(--bg-1-color);
}

p {
  font-size: 14px;
}

img {
  width: 18px;
  height: 18px;
}

span {
  font-weight: 600;
}

.block {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.info-list {
  display: flex;
  align-items: center;
  gap: 12px;
}

.info {
  display: flex;
  align-items: center;
  gap: 6px;
}
</style>
