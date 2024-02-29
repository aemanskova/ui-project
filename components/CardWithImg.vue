<template>
  <div :style="{ background: bgColor, color: color }" class="card">
    <slot class="card__img" name="img"></slot>
    <div class="card__content">
      <span class="card__header" v-if="text">{{ text }}</span>
      <p class="card__desc" v-if="paragraph">{{ paragraph }}</p>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.card {
  display: flex;
  flex-direction: column;
  gap: 20px;
  padding: 15px 15px 20px;
  border-radius: 10px;
  box-shadow: var(--card-shadow);

  &__header {
    font-size: 18px;
  }
  &__desc {
    font-size: 15px;
  }

  &__content {
    display: flex;
    flex-direction: column;
    gap: 5px;
  }
}
@media (min-width: 768px) {
  .card {
    padding: 20px 20px 25px;
    max-width: 688px;

    &__header {
      font-size: 22px;
    }
    &__desc {
      font-size: 18px;
    }
  }
}

@media (min-width: 1440px) {
  .card {
    max-width: 790px;
  }
}
</style>
      
<script setup lang="ts">
const props = defineProps({
  bgColor: { type: String, default: "defaultBgColor" },
  color: { type: String, default: "defaultColor" },
  text: { type: String, default: "defaultText" },
  paragraph: { type: String, default: "defaultParagraph" },
});
</script>