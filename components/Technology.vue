<template>
  <div class="technology">
    <div>
      <span class="technology__header">
        За каждым <ColorText textColor="var(--red)">успешным</ColorText> брендом
        стоят идеи и технология
      </span>
      <p class="technology__text">
        Последовательность действий, которая поможет создать и запустить бренд
      </p>
    </div>

    <div class="technology__cards">
      <CardWithNumber
        hoverBgColor="linear-gradient(86.57deg, #E91831 3.1%, #F67145 95.57%)"
        hoverTextColor="var(--white)"
        bgColor="var(--bg-card)"
        color="var(--main-text)"
        text="0.1       ИДЕЯ"
        paragraph="Как основатель бренда ты получишь долгосрочный сценарий развития, дорожную карту реализации и план действий сейчас на те ресурсы, что у тебя есть. Как инвестор ты получишь технологию"
        :icon="true"
      >
        <template v-slot:iconOpen>
          <svg
            width="40"
            height="40"
            viewBox="0 0 40 40"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <rect width="40" height="40" rx="20" fill="#F94747" />
            <rect x="19" y="9" width="3" height="21" fill="white" />
            <rect
              x="10"
              y="21"
              width="3"
              height="21"
              transform="rotate(-90 10 21)"
              fill="white"
            />
          </svg>
        </template>
        <template v-slot:iconClose>
          <svg
            width="40"
            height="40"
            viewBox="0 0 40 40"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <rect width="40" height="40" rx="20" fill="#F94747" />
            <rect
              x="13"
              y="13"
              width="3"
              height="21"
              transform="rotate(-45 13 13)"
              fill="white"
            />
            <rect
              x="14"
              y="28"
              width="3"
              height="21"
              transform="rotate(-135 14 28)"
              fill="white"
            />
          </svg>
        </template>
      </CardWithNumber>
      <CardWithNumber
        hoverBgColor="var(--bg-card)"
        hoverTextColor="var(--main-text)"
        bgColor="linear-gradient(86.57deg, #E91831 3.1%, #F67145 95.57%)"
        color="var(--white)"
        text="0.2       АНАЛИЗ"
        paragraph="Как основатель бренда ты получишь долгосрочный сценарий развития, дорожную карту реализации и план действий сейчас на те ресурсы, что у тебя есть. Как инвестор ты получишь технологию"
        :icon="true"
      >
        <template v-slot:iconOpen>
          <svg
            width="40"
            height="40"
            viewBox="0 0 40 40"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <rect width="40" height="40" rx="20" fill="#F94747" />
            <rect x="19" y="9" width="3" height="21" fill="white" />
            <rect
              x="10"
              y="21"
              width="3"
              height="21"
              transform="rotate(-90 10 21)"
              fill="white"
            />
          </svg>
        </template>
        <template v-slot:iconClose>
          <svg
            width="40"
            height="40"
            viewBox="0 0 40 40"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <rect width="40" height="40" rx="20" fill="#F94747" />
            <rect
              x="13"
              y="13"
              width="3"
              height="21"
              transform="rotate(-45 13 13)"
              fill="white"
            />
            <rect
              x="14"
              y="28"
              width="3"
              height="21"
              transform="rotate(-135 14 28)"
              fill="white"
            />
          </svg>
        </template>
      </CardWithNumber>
      <CardWithNumber
        hoverBgColor="linear-gradient(86.57deg, #E91831 3.1%, #F67145 95.57%)"
        hoverTextColor="var(--white)"
        bgColor="var(--bg-card)"
        color="var(--main-text)"
        text="0.3      БИЗНЕС-МОДЕЛЬ"
        paragraph="Как основатель бренда ты получишь долгосрочный сценарий развития, дорожную карту реализации и план действий сейчас на те ресурсы, что у тебя есть. Как инвестор ты получишь технологию"
        :icon="true"
      >
        <template v-slot:iconOpen>
          <svg
            width="40"
            height="40"
            viewBox="0 0 40 40"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <rect width="40" height="40" rx="20" fill="#F94747" />
            <rect x="19" y="9" width="3" height="21" fill="white" />
            <rect
              x="10"
              y="21"
              width="3"
              height="21"
              transform="rotate(-90 10 21)"
              fill="white"
            />
          </svg>
        </template>
        <template v-slot:iconClose>
          <svg
            width="40"
            height="40"
            viewBox="0 0 40 40"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <rect width="40" height="40" rx="20" fill="#F94747" />
            <rect
              x="13"
              y="13"
              width="3"
              height="21"
              transform="rotate(-45 13 13)"
              fill="white"
            />
            <rect
              x="14"
              y="28"
              width="3"
              height="21"
              transform="rotate(-135 14 28)"
              fill="white"
            />
          </svg>
        </template>
      </CardWithNumber>
    </div>
  </div>
</template>
<style lang="scss" scoped>
span,
p {
  color: var(--main-text);
}

.technology {
  &__header {
    font-size: 28px;
  }
  &__text {
    font-size: 15px;
    margin: 15px 0px 30px;
  }
  &__cards {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }
}

@media (min-width: 768px) {
  .technology {
    &__header {
      display: block;
      font-size: 54px;
      max-width: 560px;
      line-height: 54px;
    }
    &__text {
      font-size: 22px;
      max-width: 520px;
    }
    &__cards {
      gap: 20px;
    }
  }
}
@media (min-width: 1440px) {
  .technology {
    display: flex;
    justify-content: space-between;
    &__header {
      font-size: 54px;
      /* min-width: 700px; */
      line-height: 58px;
    }
    &__text {
      font-size: 18px;
      max-width: 400px;
    }
  }
}
@media (min-width: 1920px) {
  .technology {
    &__header {
      font-size: 58px;
      max-width: 700px;
    }
  }
}
</style>