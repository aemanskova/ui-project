<template>
  <div
    class="card"
    :style="dynamicStyles"
    @mouseover="setHover(true)"
    @mouseout="setHover(false)"
  >
    <span class="card__header">{{ header }}</span>
    <div class="card__content">
      <ul class="card__list">
        <li>{{ property1 }}</li>
        <li>{{ property2 }}</li>
        <li>{{ property3 }}</li>
        <li>{{ property4 }}</li>
        <li>{{ property5 }}</li>
        <li>{{ property6 }}</li>
      </ul>
      <div class="card__spans">
        <span class="card__title">
          {{ price }}
        </span>
        <span class="card__price">
          {{ textComponent }}
          <ColorText :textColor="stylePrice">{{
            colorPriceComponent
          }}</ColorText></span
        >

        <span class="card__price"
          >{{ textIndividual
          }}<ColorText :textColor="stylePrice">{{
            colorPriceIndividual
          }}</ColorText></span
        >
      </div>
    </div>
  </div>
</template>
<script setup>
const props = defineProps({
  bgColor: { type: String, default: "defaultBgColor" },
  color: { type: String, default: "defaultColor" },
  header: { type: String, default: "defaultText" },
  property1: { type: String, default: "defaultParagraph" },
  property2: { type: String, default: "defaultParagraph" },
  property3: { type: String, default: "defaultParagraph" },
  property4: { type: String, default: "defaultParagraph" },
  property5: { type: String, default: "defaultParagraph" },
  property6: { type: String, default: "defaultParagraph" },
  textComponent: { type: String, default: "defaultParagraph" },
  textIndividual: { type: String, default: "defaultParagraph" },
  colorPriceComponent: { type: String, default: "defaultParagraph" },
  colorPriceIndividual: { type: String, default: "defaultParagraph" },
  price: { type: String, default: "defaultParagraph" },
  colorPrice: { type: String, default: "defaultColor" },
  hoverBgColor: { type: String, default: "defaultBgColor" },
  hoverTextColor: { type: String, default: "defaultBgColor" },
  colorPriceHover: { type: String, default: "defaultBgColor" },
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

const stylePrice = ref(props.colorPrice);

watchEffect(() => {
  dynamicStyles.value.background = isHovered.value
    ? props.hoverBgColor
    : props.bgColor;
  dynamicStyles.value.color = isHovered.value
    ? props.hoverTextColor
    : props.color;
  stylePrice.value = isHovered.value ? props.colorPriceHover : props.colorPrice;
});
</script>
<style lang="scss" scoped>
.card {
  display: flex;
  flex-direction: column;
  gap: 20px;
  box-shadow: var(--card-shadow);
  border-radius: 10px;
  padding: 35px;
  max-width: 328px;
  &__header {
    font-size: 24px;
  }
  &__spans {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }
  &__price {
    display: flex;
    flex-direction: column;
  }
  &__price,
  &__list {
    font-size: 15px;
  }
  &__title {
    font-size: 18px;
  }
  &__content {
    display: flex;
    flex-direction: column;
    gap: 15px;
  }
  &__list {
    list-style-type: none;
    padding-left: 0;
  }
}
@media (min-width: 768px) {
  .card {
    gap: 27px;
    padding: 50px 35px;
    &__header {
      font-size: 33px;
    }
    &__price,
    &__list {
      font-size: 18px;
    }
    &__title {
      font-size: 22px;
    }

    &__content {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
  }
}
@media (min-width: 1440px) {
  .card {
    gap: 25px;
    padding: 45px 30px;
    &__header {
      font-size: 28px;
    }
    &__price,
    &__list {
      font-size: 14px;
    }
    &__title {
      font-size: 18px;
    }

    &__content {
      display: flex;
      flex-direction: column;
      gap: 15px;
    }
    max-width: 360px;
  }
}
@media (min-width: 1920px) {
  .card {
    gap: 27px;
    padding: 45px 40px;
    &__header {
      font-size: 33px;
    }
    &__price,
    &__list {
      font-size: 18px;
    }
    &__title {
      font-size: 22px;
    }

    &__content {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
  }
}
</style>