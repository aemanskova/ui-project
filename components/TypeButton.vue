<template>
  <button
    type="button"
    :class="{
      'primary-button': primary,
      'secondary-button': secondary,
      'thirdly-button': thirdly,
    }"
    :style="{ backgroundColor: color }"
  >
    {{ text }}
  </button>
</template>
<script setup lang="ts">
const props = defineProps({
  text: String,
  color: String,
  primary: Boolean,
  secondary: Boolean,
  thirdly: Boolean,
});
</script>

<style lang="scss" scoped>
button {
  border: none;
  cursor: pointer;
  color: var(--white);
  border-radius: 6px;

  &.primary-button {
    padding: 8px 30px;
    font-size: 18px;
  }

  &.secondary-button {
    padding: 16px 35px;
    font-size: 14px;
  }
  &.thirdly-button {
    padding: 10px 30px;
    font-size: 18px;
  }
}

@media (min-width: 768px) {
  button {
    &.primary-button {
      padding: 10px 30px;
    }
    &.secondary-button {
      width: max-content;
      height: max-content;
    }
    &.thirdly-button {
      width: max-content;
    }
  }
}
</style>