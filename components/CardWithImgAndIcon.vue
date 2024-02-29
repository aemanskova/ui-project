<template>
  <div
    :style="dynamicStyles"
    @mouseover="setHover(true)"
    @mouseout="setHover(false)"
    class="card"
  >
    <slot class="card__img" name="img"></slot>

    <div class="card__content">
      <div class="card__flex">
        <slot v-if="icon" name="icon"></slot>
        <span class="card__header" v-if="text">{{ text }}</span>
      </div>
      <p class="card__desc" v-if="paragraph">{{ paragraph }}</p>
    </div>
  </div>
</template>
      <style lang="scss" scoped>
.card {
  display: flex;
  flex-direction: column;
  gap: 20px;
  padding: 15px;
  border-radius: 10px;
  box-shadow: var(--card-shadow);

  &__header {
    font-size: 18px;
  }
  &__desc {
    font-size: 15px;
  }
  &__flex {
    display: flex;
    gap: 17px;
    align-items: center;
  }
  &__content {
    display: flex;
    flex-direction: column;
    gap: 10px;
    font-weight: 400;
  }
}
@media (max-width: 767px) {
  .card {
    &__flex {
      max-height: 30px;
    }
  }
}
@media (min-width: 768px) {
  .card {
    flex-direction: row;
    max-height: 245px;
    /* min-width: 688px; */
    /* &__content {
      min-width: 318px;
    } */
    &__flex {
      flex-direction: column;
      align-items: start;
      gap: 25px;
    }

    &__header {
      font-size: 22px;
    }
    &__desc {
      font-size: 14px;
    }
  }
}
@media (min-width: 1440px) {
  .card {
    &__header {
      font-size: 14px;
    }

    &__desc {
      font-size: 12px;
    }
  }
}

@media (min-width: 1920px) {
  .card {
    max-width: 790px;
    &__flex {
      gap: 50px;
    }
    &__header {
      font-size: 22px;
    }
    &__desc {
      font-size: 14px;
    }
  }
}
</style>
    
<script setup>
const props = defineProps({
  bgColor: { type: String, default: "defaultBgColor" },
  color: { type: String, default: "defaultColor" },
  text: { type: String, default: "defaultText" },
  paragraph: { type: String, default: "defaultParagraph" },
  icon: { type: Boolean, default: true },
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