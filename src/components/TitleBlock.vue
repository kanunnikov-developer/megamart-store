<script setup>
const data = defineProps({
  title: String,
  accentText: String,
  buttonText: {
    type: String,
    default: "View Al",
  },
});
</script>

<template>
  <div class="title">
    <div class="container">
      <div class="title-block">
        <div class="main-text">
          <h3>
            {{ data.title }} <span>{{ data.accentText }}</span>
          </h3>
          <button class="button">
            {{ data.buttonText }} <img src="../icons/Left.svg" alt="Left" />
          </button>
        </div>
        <div class="border"></div>
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<style scoped>
.title {
  margin-top: 30px;
}

.title-block {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

.main-text {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.button {
  color: var(--text-black-color);
  display: flex;
  align-items: center;
  gap: 6px;
  font-weight: 500;
  padding: 12px 7px 12px 15px;
  border-radius: 10px;
  transition: all 0.1s ease-in;
}

.button:hover {
  background: var(--bg-3-color);
  transition: all 0.1s ease-in;
}

h3 {
  font-size: 24px;
  font-weight: 700;
}

span {
  color: var(--primary-color);
}
</style>
