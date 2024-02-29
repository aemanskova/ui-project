<template>
  <div
    :style="dynamicStyles"
    @mouseover="setHover(true)"
    @mouseout="setHover(false)"
    class="card"
  >
    <div class="card__content">
      <slot name="icon"></slot>

      <div class="card__text">
        <span class="card__header" v-if="text">{{ text }}</span>
        <p class="card__desc" v-if="paragraph">{{ paragraph }}</p>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.card {
  display: flex;
  flex-direction: column;
  padding: 30px 20px;
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
    gap: 20px;
    font-weight: 400;
  }
  &__text {
    display: flex;
    flex-direction: column;
    gap: 5px;
    &--img {
      gap: 10px;
    }
  }
}
@media (min-width: 768px) {
  .card {
    max-width: 385px;
  }
  .card__content {
    gap: 33px;
  }
  .card__header {
    font-size: 22px;
  }
  .card__desc {
    font-size: 18px;
  }
}
</style>
    
<script setup>
const props = defineProps({
  bgColor: { type: String, default: "defaultBgColor" },
  color: { type: String, default: "defaultColor" },
  text: { type: String, default: "defaultText" },
  paragraph: { type: String, default: "defaultParagraph" },
  hoverBgColor: { type: String, default: "defaultBgColor" },
  hoverTextColor: { type: String, default: "defaultBgColor" },
});
const isHovered = ref(false);

const setHover = (value) => {
  isHovered.value = value;
  console.log("1");
  console.log(isHovered.value);
};

const dynamicStyles = ref({
  background: props.bgColor,
  color: props.color,
});

watchEffect(() => {
  dynamicStyles.value.background = isHovered.value
    ? props.hoverBgColor
    : props.bgColor;
  dynamicStyles.value.color = isHovered.value
    ? props.hoverTextColor
    : props.color;
});
</script>