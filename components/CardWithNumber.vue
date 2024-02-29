<template>
  <div
    :style="dynamicStyles"
    @mouseover="setHover(true)"
    @mouseout="setHover(false)"
    class="card"
  >
    <div class="card__header">
      <span class="card__title" v-if="text">{{ text }}</span>
      <div v-if="icon">
        <div v-if="!hasParagraph" @click="openParagraph()">
          <slot name="iconOpen"></slot>
        </div>
        <div @click="openParagraph()" v-if="hasParagraph">
          <slot name="iconClose"></slot>
        </div>
      </div>
    </div>
    <p class="card__text" v-if="hasParagraph">{{ paragraph }}</p>
  </div>
</template>
  <style lang="scss" scoped>
.card {
  padding: 20px;
  border-radius: 10px;
  font-weight: 400;
  box-shadow: var(--card-shadow);

  &__header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 22px;
    line-height: 28.05px;
  }
  &__text {
    font-size: 18px;
  }
}
@media (min-width: 1440px) {
  .card {
    width: 460px;
  }
}
@media (min-width: 1920px) {
  .card {
    width: 790px;
  }
}
</style>
  
<script setup >
const props = defineProps({
  bgColor: { type: String, default: "defaultBgColor" },
  color: { type: String, default: "defaultColor" },
  text: { type: String, default: "defaultText" },
  paragraph: { type: String, default: "defaultParagraph" },
  icon: { type: Boolean, default: false },
  hoverBgColor: { type: String, default: "defaultBgColor" },
  hoverTextColor: { type: String, default: "defaultBgColor" },
});
const hasParagraph = ref(false);

function openParagraph() {
  hasParagraph.value = !hasParagraph.value;
}

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

  