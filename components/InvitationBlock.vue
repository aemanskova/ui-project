<template>
  <div class="invitation">
    <span class="invitation__header"
      ><ColorText textColor="var(--yellow)">Приглашаем</ColorText> в команду
      PHP-разработчика</span
    >
    <CardWithButton
      class="invitation__card"
      paragraph="Lorem Ipsum (читается как «Лорем Ипсум») — это текст-заглушка, текст-рыба, обычно используемый дизайнерами и веб-разработчиками для демонстрации того, в каких местах сайта или приложения будет ."
      span="Готов прислать резюме?"
      bgColor="linear-gradient(119.66deg, #F68743 3.73%, #FDBD34 92.86%)"
      color="var(--white)"
    />
    <p class="invitation__text">
      Lorem Ipsum (читается как «Лорем Ипсум») — это текст-заглушка, текст-рыба,
      обычно используемый дизайнерами и веб-разработчиками для демонстрации
      того, в каких местах сайта или приложения будет находиться текст, какого
      он будет объема и каким шрифтом написан. Lorem Ipsum (читается как «Лорем
      Ипсум») — это текст-заглушка, текст-рыба, обычно используемый дизайнерами
      и веб-разработчиками для демонстрации того, в каких местах сайта или
      приложения будет находиться текст, какого он будет объема и каким шрифтом
      написан. Lorem Ipsum (читается как «Лорем Ипсум») — это текст-заглушка,
      текст-рыба, обычно используемый дизайнерами и веб-разработчиками для
      демонстрации того, в каких местах сайта или приложения будет находиться
      текст, какого он будет объема и каким шрифтом написан.
    </p>

    <img src="/img/man-front-of-pc.png" alt="A man sitting front of computer" />
    <p class="invitation__text">
      Lorem Ipsum (читается как «Лорем Ипсум») — это текст-заглушка, текст-рыба,
      обычно используемый дизайнерами и веб-разработчиками для демонстрации
      того, в каких местах сайта или приложения будет находиться текст, какого
      он будет объема и каким шрифтом написан. Lorem Ipsum (читается как «Лорем
      Ипсум») — это текст-заглушка, текст-рыба, обычно используемый дизайнерами
      и веб-разработчиками для демонстрации того, в каких местах сайта или
      приложения будет находиться текст, какого он будет объема и каким шрифтом
      написан. Lorem Ipsum (читается как «Лорем Ипсум») — это текст-заглушка,
      текст-рыба, обычно используемый дизайнерами и веб-разработчиками для
      демонстрации того, в каких местах сайта или приложения будет находиться
      текст, какого он будет объема и каким шрифтом написан.
    </p>

    <PaginationNumbers class="invitation__pag" />
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
  max-width: 790px;
  margin: 20px 0px;
}
.invitation {
  max-width: 790px;
  margin: 0 auto;
  &__header {
    display: block;
    margin-bottom: 30px;
    font-size: 28px;
  }
  &__text {
    font-size: 15px;
  }
  &__card {
    max-width: 790px;
    margin-bottom: 20px;
  }
  &__pag {
    margin-top: 30px;
    float: right;
  }
}
@media (min-width: 768px) {
  .invitation {
    &__header {
      display: block;
      font-size: 54px;
      margin-bottom: 40px;
      max-width: 687px;
      line-height: 54px;
    }
    &__pag {
      margin-top: 70px;
    }
    &__text {
      font-size: 18px;
    }
    &__card {
      margin-bottom: 30px;
    }
  }
  img {
    margin: 30px 0px;
  }
}
@media (min-width: 1440px) {
  .invitation {
    &__header {
      font-size: 58px;
      margin-bottom: 60px;
      line-height: 58px;
    }
    &__text {
      display: block;
      max-width: 785px;
    }
    &__card {
      margin-bottom: 50px;
    }
  }
}
</style>