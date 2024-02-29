<template>
  <div class="gallery-page">
    <div>
      <span class="gallery-page__header"
        >Примеры <ColorText textColor="var(--yellow)">контента</ColorText></span
      >
      <p class="gallery-page__text">
        Посмотрите, как мы работаем с UX/UI дизайном и структурируем смыслы
      </p>
    </div>

    <GalleryLikeInPinterest />
    <TypeButton
      class="gallery-page__button"
      thirdly
      color="var(--yellow)"
      text="Загрузить еще"
    ></TypeButton>
  </div>
</template>

<style lang="scss" scoped>
.gallery-page {
  display: flex;
  flex-direction: column;
  color: var(--main-text);
  &__header {
    font-size: 28px;
  }
  &__text {
    font-size: 15px;
    margin: 15px 0px 30px;
  }
  &__button {
    margin: 30px auto 0px;
  }
}
@media (min-width: 768px) {
  .gallery-page {
    &__text {
      font-size: 18px;
      margin: 20px 0px 40px;
    }
    &__header {
      font-size: 54px;
    }
    &__button {
      margin: 36px auto 0px;
    }
  }
}
@media (min-width: 1440px) {
  .gallery-page {
    &__header {
      font-size: 58px;
    }
    &__text {
      margin: 15px 0px 60px;
    }
    &__button {
      margin: 70px auto 0px;
    }
  }
}
</style>