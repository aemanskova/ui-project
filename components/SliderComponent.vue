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
    :space-between="20"
    :freeMode="true"
    :breakpoints="breakpoints"
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
  cards: { type: Boolean, default: false },
  services: { type: Boolean, default: false },
  paginate: { type: Boolean, default: false },
});

const pagination = computed(() => {
  if (props.paginate) {
    return true;
  } else return false;
});

const breakpoints = computed(() => {
  if (props.cards) {
    return {
      360: {
        slidesPerView: 1,
      },
      1440: {
        slidesPerView: 2,
        spaceBetween: 40,
      },
    };
  } else if (props.services) {
    return {
      360: {
        slidesPerView: 1,
      },
      650: {
        slidesPerView: 2,
        spaceBetween: 20,
      },
      1000: {
        slidesPerView: 3,
        spaceBetween: 20,
      },
      1500: {
        slidesPerView: 4,
        spaceBetween: 20,
      },
    };
  }
});
</script>
<style lang="scss" scoped>
.swiper-pagination-bullet-active {
  background-color: var(-purple) !important;
}
.mySwiper {
  padding-bottom: 50px;
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