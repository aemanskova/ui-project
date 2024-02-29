<template>
  <div
    :id="id"
    tabindex="-1"
    aria-hidden="true"
    class="hidden overflow-y-auto overflow-x-hidden fixed top-0 right-0 left-0 z-50 justify-center items-center w-full md:inset-0 h-[calc(100%-1rem)] max-h-full"
  >
    <div
      class="modal modal-video relative rounded-lg p-2 w-full max-w-2xl max-h-full shadow"
    >
      <div class="modal__header flex items-center justify-between">
        <button
          type="button"
          class="ms-auto inline-flex justify-center items-center"
          :data-modal-hide="id"
        >
          <svg
            width="20"
            height="20"
            viewBox="0 0 20 20"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <rect width="20" height="20" rx="2" fill="#B822ED" />
            <path
              d="M15 15L5 5M15 5L5 15"
              stroke="white"
              stroke-width="2"
              stroke-linecap="round"
            />
          </svg>
        </button>
      </div>
      <div class="modal__body">
        <div class="modal-video__video"><slot name="video"></slot></div>
      </div>
    </div>
  </div>
</template>
    <script setup>
import "flowbite";

const props = defineProps({
  id: { type: String, default: "default-modal" },
});
</script>
<style lang="scss">
.modal-video {
  min-width: 90vw;
  &__video {
    justify-content: center;
    display: flex;
  }
}
</style>
