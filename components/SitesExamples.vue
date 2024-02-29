<template>
  <div class="examples">
    <div class="examples__desc">
      <span class="examples__header"
        ><ColorText textColor="var(--red)">Примеры</ColorText> сайтов</span
      >
      <p class="examples__text">
        Посмотрите, как мы работаем с UX/UI дизайном и структурируем смыслы
      </p>
    </div>

    <SliderComponent paginate cards arrows>
      <SwiperSlide>
        <CardSite
          bgColor="linear-gradient(86.57deg, #E91831 3.1%, #F67145 95.57%)"
          color="var(--white)"
          title="Русмастер"
          text="Интернет-магазин 2023"
        >
          <img src="/img/first-site-example.png" alt="" />
        </CardSite>
      </SwiperSlide>
      <SwiperSlide>
        <CardSite
          bgColor="linear-gradient(86.57deg, #E91831 3.1%, #F67145 95.57%)"
          color="var(--white)"
          title="Astilavin"
          text="Интернет-магазин 2023"
        >
          <img src="/img/second-site-example.png" alt="" />
        </CardSite>
      </SwiperSlide>
      <SwiperSlide>
        <CardSite
          bgColor="linear-gradient(86.57deg, #E91831 3.1%, #F67145 95.57%)"
          color="var(--white)"
          title="Русмастер"
          text="Интернет-магазин 2023"
        >
          <img src="/img/first-site-example.png" alt="" />
        </CardSite>
      </SwiperSlide>
      <SwiperSlide>
        <CardSite
          bgColor="linear-gradient(86.57deg, #E91831 3.1%, #F67145 95.57%)"
          color="var(--white)"
          title="Русмастер"
          text="Интернет-магазин 2023"
        >
          <img src="/img/first-site-example.png" alt="" />
        </CardSite>
      </SwiperSlide>
    </SliderComponent>
  </div>
</template>

<style lang="scss" scoped>
span,
p {
  color: var(--main-text);
}
img {
  border-radius: 10px;
}
.examples {
  &__header {
    font-size: 28px;
  }
  &__text {
    font-size: 15px;
    margin: 15px 0px 30px;
  }
}
@media (min-width: 768px) {
  .examples {
    &__header {
      font-size: 54px;
      line-height: 54px;
    }
    &__text {
      font-size: 18px;
    }
  }
}
@media (min-width: 1440px) {
  .examples {
    &__header {
      font-size: 58px;
      line-height: 58px;
    }
  }
}
</style>

