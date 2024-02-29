<template>
  <div :style="{ background: bgColor, color: color }" class="card">
    <div v-if="img">
      <slot name="img"></slot>
    </div>
    <div class="card__desc">
      <span class="card__header">{{ header }}</span>
      <p class="card__text">{{ text }}</p>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from "vue";

const props = defineProps({
  bgColor: { type: String, default: "#B822ED" },
  color: { type: String, default: "#ffffff" },
  text: { type: String, default: "defaultText" },
  header: { type: String, default: "defaultText" },
  img: { type: Boolean, default: "false" },
});
</script>
<style lang="scss" scoped>
.card {
  display: flex;
  flex-direction: column;
  gap: 15px;
  padding: 15px;
  border-radius: 10px;
  &__desc {
    display: flex;
    flex-direction: column;
    gap: 5px;
  }
  &__header {
    font-weight: 500;
    font-size: 28px;
  }
  &__text {
    font-size: 18px;
  }
}
@media (min-width: 768px) {
  .card {
    background: linear-gradient(
      86.54deg,
      #ab51ba 3.76%,
      #496bda 95.35%
    ) !important;
    padding: 25px;
    gap: 20px;
    &__desc {
      gap: 10px;
    }
    &__header {
      font-size: 52px;
      line-height: 54px;
    }
  }
}
@media (min-width: 1200px) {
  .card {
    flex-direction: row-reverse;
    justify-content: space-between;
    padding: 40px;
    &__header {
      font-size: 58px;
      max-width: 700px;
      line-height: 58px;
    }
    &__text {
      max-width: 500px;
    }
    &__desc {
      gap: 155px;
    }
  }
}
</style>