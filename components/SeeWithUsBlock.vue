<template>
  <div class="job">
    <div class="job__desc">
      <span class="job__header"
        >Кого мы хотим <ColorText textColor="var(--purple)">видеть</ColorText> с
        нами?</span
      >
      <p class="job__text">
        Lorem Ipsum (читается как «Лорем Ипсум») — это текст-заглушка,
        текст-рыба, обычно используемый дизайнерами и веб-разработчиками для
        демонстрации того, в каких местах сайта или приложения будет находиться
        текст, какого он
      </p>
    </div>

    <CardWithImg
      class="job__card"
      bgColor="linear-gradient(86.54deg, #AB51BA 3.76%, #496BDA 95.35%)"
      color="var(--white)"
      text="Разрабочик PHP"
      paragraph="Lorem Ipsum (читается как «Лорем Ипсум») — это текст-заглушка, текст-рыба, обычно используемый дизайнерами и веб-разработчиками для демонстрации того, в каких местах сайта или приложения будет находиться текст, какого он будет."
      ><template v-slot:img>
        <img
          src="/img/man-front-of-pc.png"
          alt="A man sitting front of computer" /></template
    ></CardWithImg>
  </div>
</template>
  <style lang="scss" scoped>
span,
p {
  color: var(--main-text);
}
img {
  object-fit: cover;
  width: 100%;
  border-radius: 10px;
}
.job {
  max-width: 790px;
  margin: 0 auto;
  &__header {
    font-size: 28px;
  }
  &__text {
    font-size: 15px;
    margin: 15px 0px 30px;
  }
  &__card {
    max-width: 790px;
  }
}
@media (min-width: 768px) {
  .job {
    &__header {
      display: block;
      font-size: 54px;
      max-width: 500px;
      line-height: 54px;
    }
    &__text {
      font-size: 18px;
      margin: 20px 0px 40px;
    }
  }
}
@media (min-width: 1440px) {
  .job {
    &__header {
      font-size: 58px;
      line-height: 58px;
    }
    &__text {
      display: block;
      max-width: 680px;
      margin: 60px 0px 30px;
    }
  }
}
</style>