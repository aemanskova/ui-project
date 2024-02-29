<template>
  <div class="arrows" v-if="arrows">
    <button class="slider__prev">
      <svg
        width="50"
        height="50"
        viewBox="0 0 50 50"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <rect
          width="50"
          height="50"
          rx="25"
          transform="matrix(-1 0 0 1 50 0)"
          fill="#F94747"
        />
        <path d="M29 34L20 25L29 16" stroke="white" stroke-width="2" />
      </svg>
    </button>
    <button class="slider__next">
      <svg
        width="50"
        height="50"
        viewBox="0 0 50 50"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <rect width="50" height="50" rx="25" fill="#F94747" />
        <path d="M21 34L30 25L21 16" stroke="white" stroke-width="2" />
      </svg>
    </button>
  </div>

  <Swiper
    class="mySwiper"
    :modules="[SwiperNavigation, SwiperPagination, SwiperFreeMode]"
    :loop="true"
    :slides-per-view="2.2"
    :breakpoints="breakpoints"
    :free-mode="true"
    :centered-slides="false"
    :space-between="10"
    :navigation="{
      nextEl: '.slider__next',
      prevEl: '.slider__prev',
    }"
    :pagination="pagination"
  >
    <slot></slot>
  </Swiper>
</template>
  <script setup lang="ts">
const props = defineProps({
  arrows: { type: Boolean, default: false },
  paginate: { type: Boolean, default: false },
});

const pagination = computed(() => {
  if (props.paginate) {
    return true;
  } else return false;
});
const breakpoints = computed(() => {
  return {
    360: {
      slidesPerView: 1,
    },
    860: {
      slidesPerView: 1.1,
      spaceBetween: 5,
    },
    1440: {
      slidesPerView: 2.2,
      spaceBetween: 10,
    },
  };
});
</script>
  <style lang="scss" scoped>
.swiper-pagination-bullet-active {
  background-color: var(-purple) !important;
}
.mySwiper {
  padding-bottom: 50px;
  /* margin-left: calc(-50% + 50px); */
  --swiper-pagination-color: var(--purple);
  --swiper-pagination-bullet-inactive-color: var(--purple);
  --swiper-pagination-bullet-inactive-opacity: 0.6;
}

.active {
  opacity: 50%;
}
.arrows {
  display: flex;
  gap: 8px;
  margin-bottom: 15px;
  margin-left: calc(100% - 108px);
}
@media (min-width: 768px) {
  .arrows {
    margin-bottom: 38px;
  }
}
@media (min-width: 1440px) {
  .arrows {
    margin-bottom: 58px;
  }
}
</style>