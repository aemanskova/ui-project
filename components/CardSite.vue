<template>
  <div class="card" :style="{ background: bgColor, color: color }">
    <slot></slot>
    <div class="card__desc">
      <span class="card__title">{{ title }}</span>
      <span class="card__text">{{ text }}</span>
    </div>
  </div>
</template>
<script setup lang="ts">
const props = defineProps<{
  bgColor: string;
  color: string;
  title: string;
  text: string;
}>();
</script>
<style lang="scss" scoped>
.card {
  border-radius: 10px;
  padding: 20px 20px 30px;
  display: flex;
  flex-direction: column;
  gap: 10px;
  max-width: 790px;
  &__desc {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  &__title {
    font-size: 18px;
  }
  &__text {
    font-size: 15px;
  }
}
@media (min-width: 768px) {
  .card {
    gap: 15px;
    &__title {
      font-size: 22px;
    }
    &__text {
      font-size: 18px;
    }
  }
}
</style>