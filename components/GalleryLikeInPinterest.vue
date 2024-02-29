<template>
  <div
    class="gallery columns-2 min-[768px]:columns-3 min-[768px]:columns-3 min-[1440px]:columns-4 max-w-7xl mx-auto space-y-4"
  >
    <div
      class="gallery__img rounded-md overflow-hidden"
      @mouseenter="playVideo"
      @mouseleave="pauseVideo"
      data-modal-target="modal-video-popup"
      data-modal-toggle="modal-video-popup"
    >
      <a>
        <div class="video">
          <iframe
            class="video__iframe"
            ref="videoFrame"
            :src="videoUrl"
            frameborder="0"
            allowfullscreen
          >
          </iframe>
          <svg
            class="video__play-btn"
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
        </div>
      </a>
    </div>
    <ModalVideo id="modal-video-popup">
      <template v-slot:video>
        <iframe
          class="modal--video"
          src="https://www.youtube.com/embed/fctpipvvEqc?rel=0&showinfo=0"
          frameborder="0"
          allowfullscreen
        ></iframe>
      </template>
    </ModalVideo>
    <div class="gallery__img rounded-md overflow-hidden">
      <a
        data-modal-target="modal-photo-cheerful"
        data-modal-toggle="modal-photo-cheerful"
      >
        <img src="/img/cheerful-girl.jpg" alt="Cheerful girl with curly hair"
      /></a>
    </div>

    <div class="gallery__img rounded-md overflow-hidden">
      <a
        data-modal-target="modal-photo-business-lady"
        data-modal-toggle="modal-photo-business-lady"
      >
        <img src="/img/business-lady.jpg" alt="Business girl"
      /></a>
    </div>
    <div class="gallery__img gallery__img--tablet rounded-md overflow-hidden">
      <a
        data-modal-target="modal-photo-blue"
        data-modal-toggle="modal-photo-blue"
      >
        <img src="/img/girl-in-blue.jpg" alt="Beautiful girl in blue clothes"
      /></a>
    </div>

    <div class="gallery__img gallery__img--tablet rounded-md overflow-hidden">
      <a
        data-modal-target="modal-photo-blue"
        data-modal-toggle="modal-photo-blue"
      >
        <img src="/img/girl-in-blue.jpg" alt="Beautiful girl in blue clothes" />
      </a>
    </div>

    <div class="gallery__img gallery__img--tablet rounded-md overflow-hidden">
      <a
        data-modal-target="modal-photo-cheerful"
        data-modal-toggle="modal-photo-cheerful"
      >
        <img src="/img/cheerful-girl.jpg" alt="Cheerful girl with curly hair"
      /></a>
    </div>

    <div class="gallery__img gallery__img--pc rounded-md overflow-hidden">
      <a
        data-modal-target="modal-photo-business-lady"
        data-modal-toggle="modal-photo-business-lady"
      >
        <img src="/img/business-lady.jpg" alt="Business girl"
      /></a>
    </div>

    <div class="gallery__img gallery__img--pc rounded-md overflow-hidden">
      <a
        data-modal-target="modal-photo-red-haired-girl"
        data-modal-toggle="modal-photo-red-haired-girl"
      >
        <img src="/img/red-haired-girl.jpg" alt="Girl with red hair in beret"
      /></a>
    </div>
  </div>

  <ModalPhoto id="modal-photo-business-lady"
    ><template v-slot:img>
      <img src="/img/business-lady.jpg" alt="Business girl" /> </template
  ></ModalPhoto>
  <ModalPhoto id="modal-photo-red-haired-girl"
    ><template v-slot:img>
      <img
        src="/img/red-haired-girl.jpg"
        alt="Girl with red hair in beret"
      /> </template
  ></ModalPhoto>
  <ModalPhoto id="modal-photo-cheerful"
    ><template v-slot:img>
      <img
        src="/img/cheerful-girl.jpg"
        alt="Cheerful girl with curly hair"
      /> </template
  ></ModalPhoto>
  <ModalPhoto id="modal-photo-blue"
    ><template v-slot:img>
      <img
        src="/img/girl-in-blue.jpg"
        alt="Beautiful girl in blue clothes"
      /> </template
  ></ModalPhoto>
</template>
<script setup>
const videoUrl = ref(
  "https://www.youtube.com/embed/fctpipvvEqc?rel=0&showinfo=0&autoplay=0"
);

const playVideo = () => {
  videoUrl.value = videoUrl.value.replace("&autoplay=0", "&autoplay=1");
};

const pauseVideo = () => {
  videoUrl.value = videoUrl.value.replace("&autoplay=1", "&autoplay=0");
};
</script>
<style lang="scss" scoped>
.modal--video {
  width: 100%;
  height: 80vh;
}
.video {
  position: relative;
  width: 100%;
  &__iframe {
    min-width: 159px;
    width: 100%;
  }
  &__play-btn {
    position: absolute;
    bottom: 10px;
    right: 10px;
  }
}
img {
  max-height: 90vh;
  object-fit: contain;
}
@media (max-width: 768px) {
  a {
    display: block;
  }

  .gallery {
    &__img {
      &--tablet {
        display: none;
      }
    }
  }
}
@media (max-width: 1440px) {
  .gallery {
    &__img {
      &--pc {
        display: none;
      }
    }
  }
}
</style>