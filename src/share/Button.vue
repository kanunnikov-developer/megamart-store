<script setup></script>

<template>
  <button><slot></slot></button>
</template>

<style scoped>
button {
  color: var(--primary-color);
  padding: 12px 15px;
  border-radius: 10px;
  transition: all 0.1s ease-in;
  border: 1px solid var(--primary-color);
}

button:hover {
  background: var(--bg-3-color);
  transition: all 0.1s ease-in;
}
</style>
