<template>
  <div class="banner">
    <div class="banner__title">
      <div class="banner__img-box">
        <img
          class="banner__img"
          srcset="
            /img/banner-img-mobile.jpg 320w,
            /img/banner-img-tablet.jpg 480w,
            /img/banner-img-pk.jpg     800w
          "
          sizes="(max-width: 360px) 328px,
            (max-width: 768px) 688px,
            800px"
          src="/img/banner-img-pk.jpg"
          alt="Photo of the head of the company"
        />
        <button
          data-modal-target="modal-video-mobile"
          data-modal-toggle="modal-video-mobile"
          type="button"
          class="banner__play-btn"
        >
          <svg
            width="51"
            height="51"
            viewBox="0 0 51 51"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <circle cx="25.6155" cy="25.6152" r="25" fill="#FF8718" />
            <path
              d="M31.1766 25.3623C31.634 25.6457 31.634 26.3542 31.1766 26.6376L23.4579 31.4197C23.0005 31.7031 22.4287 31.3488 22.4287 30.7821L22.4287 21.2178C22.4287 20.6511 23.0005 20.2968 23.4579 20.5802L31.1766 25.3623Z"
              fill="#E5E5E5"
            />
          </svg>
        </button>
        <ModalVideo id="modal-video-mobile">
          <template v-slot:video>
            <iframe
              width="560"
              height="315"
              src="https://www.youtube.com/embed/fctpipvvEqc?rel=0&showinfo=0&autoplay=1"
              frameborder="0"
              allowfullscreen
            ></iframe>
          </template>
        </ModalVideo>
      </div>

      <h1 class="banner__header">
        Стань частью
        <ColorText textColor="var(--purple)">команды</ColorText>
        профессионалов
      </h1>
    </div>

    <div class="banner__content">
      <p class="banner__text banner__text--main">
        Развивайся, как специалист, решая интересные задачи. Будь в команде и
        работай на себя!
      </p>
      <span class="banner__text">Готов прислать резюме?</span>

      <div class="banner__buttons">
        <TypeButton
          data-modal-target="modal-form"
          data-modal-toggle="modal-form"
          secondary
          color="var(--red)"
          text="Связаться"
        />
        <div class="banner__play">
          <button
            data-modal-target="modal-video"
            data-modal-toggle="modal-video"
            type="button"
          >
            <svg
              width="65"
              height="65"
              viewBox="0 0 65 65"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <circle cx="32.5" cy="32.5" r="32.5" fill="#FF8718" />
              <path
                d="M39.2294 31.6711C39.824 32.0395 39.824 32.9605 39.2294 33.3289L29.1951 39.5457C28.6005 39.9141 27.8572 39.4536 27.8572 38.7168L27.8572 26.2833C27.8572 25.5465 28.6005 25.086 29.1951 25.4544L39.2294 31.6711Z"
                fill="#E5E5E5"
              />
            </svg>
          </button>
          <ModalVideo id="modal-video">
            <template v-slot:video>
              <iframe
                width="760"
                height="700"
                src="https://www.youtube.com/embed/fctpipvvEqc?rel=0&showinfo=0&autoplay=1"
                frameborder="0"
                allowfullscreen
              ></iframe>
            </template>
          </ModalVideo>
          <ModalForm></ModalForm>
          <span>Посмотрите видео о нас</span>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
iframe {
  width: 100%;
}
.banner {
  &__img-box {
    margin-top: 15px;
    position: relative;
  }
  &__play-btn {
    position: absolute;
    right: 15px;
    bottom: 15px;
  }
  &__img {
    object-fit: cover;
    width: 100%;

    border-radius: 10px;
  }
  &__content {
    color: var(--main-text);
    display: flex;
    flex-direction: column;
    gap: 15px;
  }

  &__text {
    font-weight: 400;
    font-size: 18px;
    max-width: 577px;
  }
  &__header {
    color: var(--main-text);
    font-weight: 500;
    font-size: 36px;
    line-height: 34.2px;
    margin: 15px 0;
    max-width: 894px;
  }
  &__play {
    display: none;
  }
}
@media (min-width: 768px) {
  .banner {
    &__play-btn {
      display: none;
    }
    &__img {
      max-height: 690px;
    }
    &__header {
      font-size: 60px;
      line-height: 57px;
    }
    &__text--main {
      font-size: 22px;
    }
    &__play {
      display: flex;
      align-items: center;
      gap: 22px;
    }
    &__buttons {
      display: flex;
      justify-content: space-between;
    }
  }
}

@media (min-width: 1440px) {
  .banner {
    display: flex;
    flex-direction: row-reverse;
    justify-content: space-between;
    gap: 56px;
    width: 100%;
    &__buttons {
      flex-direction: column;
      height: 100%;
    }

    &__text {
      min-width: 350px;
    }
    &__content {
      margin-top: 144px;
    }
    &__img-box {
      margin-top: 0px;
    }
    &__img {
      object-fit: cover;
      width: 100%;
      margin-top: 0px;
    }
    &__title {
      display: flex;
      flex-direction: column-reverse;
    }
  }
}
</style>