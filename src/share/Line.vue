<script setup>
const props = defineProps({
  height: {
    type: String,
    default: "20",
  },
});
</script>

<template>
  <div :style="{ height: height + 'px' }" class="line"></div>
</template>

<style scoped>
.line {
  width: 1px;
  background: #d9d9d9;
}
</style>
