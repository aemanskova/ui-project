<template>
  <div
    id="modal-form"
    tabindex="-1"
    aria-hidden="true"
    class="hidden overflow-y-auto overflow-x-hidden fixed top-0 right-0 left-0 z-50 justify-center items-center w-full md:inset-0 h-[calc(100%-1rem)] max-h-full"
  >
    <div
      class="modal relative rounded-lg p-4 w-full max-w-2xl max-h-full shadow"
    >
      <div class="modal__header flex items-center justify-between">
        <button
          type="button"
          class="ms-auto inline-flex justify-center items-center"
          data-modal-hide="modal-form"
        >
          <svg
            width="40"
            height="40"
            viewBox="0 0 40 40"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <rect width="40" height="40" rx="4" fill="#B822ED" />
            <path
              d="M30 30L10 10M30 10L10 30"
              stroke="white"
              stroke-width="2"
              stroke-linecap="round"
            />
          </svg>
        </button>
      </div>

      <div class="modal__body">
        <div class="modal__text">
          <span class="modal__title">Рассчитать проект</span>
          <span class="modal__span">Чтобы рассчитать проект....</span>
        </div>
        <div class="modal__info">
          <div class="modal__contact">
            <span class="modal__phone">+7 495 ХХХ-ХХ-ХХ</span>
            <div class="modal__icons">
              <svg
                width="26"
                height="27"
                viewBox="0 0 26 27"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M13.0033 0H12.9967C5.82888 0 0 5.93174 0 13.2257C0 16.1189 0.9165 18.8004 2.47487 20.9777L0.85475 25.891L5.85162 24.2659C7.90725 25.6513 10.3594 26.4515 13.0033 26.4515C20.1711 26.4515 26 20.5181 26 13.2257C26 5.9334 20.1711 0 13.0033 0Z"
                  fill="#FF8718"
                />
                <path
                  d="M20.5669 18.6761C20.2533 19.5771 19.0085 20.3244 18.0157 20.5426C17.3364 20.6897 16.4492 20.8071 13.4624 19.5473C9.64204 17.9371 7.18179 13.9876 6.99004 13.7313C6.80641 13.4751 5.44629 11.64 5.44629 9.74212C5.44629 7.84422 6.39366 6.92007 6.77554 6.5233C7.08916 6.19762 7.60754 6.04883 8.10479 6.04883C8.26566 6.04883 8.41029 6.05709 8.54029 6.06371C8.92216 6.08024 9.11391 6.10338 9.36579 6.71673C9.67941 7.48547 10.4432 9.38337 10.5342 9.57845C10.6268 9.77353 10.7194 10.038 10.5894 10.2943C10.4675 10.5588 10.3603 10.6762 10.1685 10.901C9.97679 11.1259 9.79479 11.2978 9.60304 11.5392C9.42754 11.7491 9.22929 11.974 9.45029 12.3625C9.67129 12.7427 10.435 14.0107 11.5595 15.0291C13.0107 16.3434 14.1872 16.7633 14.608 16.9419C14.9217 17.0741 15.2954 17.0427 15.5245 16.7947C15.8154 16.4757 16.1745 15.9466 16.5402 15.4259C16.8002 15.0522 17.1284 15.006 17.4729 15.1382C17.8239 15.2622 19.6813 16.1963 20.0632 16.3897C20.445 16.5848 20.6969 16.6774 20.7895 16.841C20.8805 17.0047 20.8805 17.7734 20.5669 18.6761Z"
                  fill="#1B1C27"
                />
              </svg>
              <svg
                width="26"
                height="26"
                viewBox="0 0 26 26"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <mask id="path-1-inside-1_1840_152" fill="white">
                  <path
                    d="M10.4456 17.0347L10.0221 23.9276C10.628 23.9276 10.8904 23.6264 11.2051 23.2647L14.0457 20.1232L19.9317 25.1114C21.0112 25.8076 21.7718 25.441 22.063 23.9622L25.9265 3.01201L25.9276 3.01077C26.27 1.16412 25.3505 0.441995 24.2988 0.895018L1.58888 10.9566C0.0389717 11.6528 0.0624389 12.6526 1.3254 13.1057L7.13141 15.1955L20.6176 5.43019C21.2523 4.94384 21.8294 5.21293 21.3547 5.69929L10.4456 17.0347Z"
                  />
                </mask>
                <path
                  d="M10.4456 17.0347L10.0221 23.9276C10.628 23.9276 10.8904 23.6264 11.2051 23.2647L14.0457 20.1232L19.9317 25.1114C21.0112 25.8076 21.7718 25.441 22.063 23.9622L25.9265 3.01201L25.9276 3.01077C26.27 1.16412 25.3505 0.441995 24.2988 0.895018L1.58888 10.9566C0.0389717 11.6528 0.0624389 12.6526 1.3254 13.1057L7.13141 15.1955L20.6176 5.43019C21.2523 4.94384 21.8294 5.21293 21.3547 5.69929L10.4456 17.0347Z"
                  fill="#FF8718"
                />
                <path
                  d="M10.4456 17.0347L-4.92566 2.24167L-10.3664 7.8951L-10.8476 15.7266L10.4456 17.0347ZM10.0221 23.9276L-11.271 22.6194L-12.6621 45.2609H10.0221V23.9276ZM11.2051 23.2647L-4.61869 8.95675L-4.75549 9.10804L-4.88936 9.26191L11.2051 23.2647ZM14.0457 20.1232L27.8383 3.84817L12.0777 -9.50842L-1.77809 5.81521L14.0457 20.1232ZM19.9317 25.1114L6.13916 41.3864L7.20031 42.2857L8.36924 43.0396L19.9317 25.1114ZM22.063 23.9622L42.9943 28.084L43.0192 27.9577L43.0425 27.8312L22.063 23.9622ZM25.9265 3.01201L9.78006 -10.9308L5.99678 -6.54962L4.94696 -0.856974L25.9265 3.01201ZM25.9276 3.01077L42.0741 16.9536L45.8501 12.5808L46.9034 6.90012L25.9276 3.01077ZM24.2988 0.895018L15.8594 -18.6981L15.7581 -18.6544L15.6572 -18.6097L24.2988 0.895018ZM1.58888 10.9566L-7.05266 -8.54817L-7.10261 -8.52604L-7.15244 -8.50365L1.58888 10.9566ZM1.3254 13.1057L8.55041 -6.96697L8.53934 -6.97095L8.52828 -6.97492L1.3254 13.1057ZM7.13141 15.1955L-0.0935964 35.2681L10.5128 39.0858L19.6432 32.4746L7.13141 15.1955ZM20.6176 5.43019L33.1293 22.7093L33.3638 22.5396L33.5935 22.3635L20.6176 5.43019ZM21.3547 5.69929L6.08762 -9.20132L6.03532 -9.14773L5.9834 -9.09378L21.3547 5.69929ZM-10.8476 15.7266L-11.271 22.6194L31.3153 25.2358L31.7388 18.3429L-10.8476 15.7266ZM10.0221 45.2609C14.3315 45.2609 18.7063 44.0503 22.5605 41.4795C24.2174 40.3744 25.4116 39.2587 26.1321 38.531C26.4945 38.1651 26.7816 37.8511 26.9624 37.6497C27.1312 37.4617 27.2796 37.2905 27.2996 37.2676L-4.88936 9.26191C-5.42924 9.88243 -3.7339 7.73102 -1.11488 5.98413C2.37804 3.65436 6.31869 2.59427 10.0221 2.59427V45.2609ZM27.0289 37.5727L29.8695 34.4312L-1.77809 5.81521L-4.61869 8.95675L27.0289 37.5727ZM0.253158 36.3982L6.13916 41.3864L33.7243 8.83636L27.8383 3.84817L0.253158 36.3982ZM8.36924 43.0396C11.3555 44.9655 20.6536 49.7741 31.1973 44.2472C40.4585 39.3927 42.5155 30.5153 42.9943 28.084L1.13161 19.8404C1.31918 18.8878 2.85035 10.9332 11.3886 6.45759C21.2094 1.30967 29.5874 5.95345 31.4942 7.18319L8.36924 43.0396ZM43.0425 27.8312L46.9061 6.88099L4.94696 -0.856974L1.0834 20.0932L43.0425 27.8312ZM42.073 16.9549L42.0741 16.9536L9.78113 -10.9321L9.78006 -10.9308L42.073 16.9549ZM46.9034 6.90012C47.6067 3.10683 48.247 -5.65931 41.5089 -13.1629C33.4401 -22.1485 22.3097 -21.4764 15.8594 -18.6981L32.7381 20.4881C27.3396 22.8134 17.1947 23.6201 9.76303 15.344C3.66209 8.54981 4.59085 1.06806 4.95179 -0.878574L46.9034 6.90012ZM15.6572 -18.6097L-7.05266 -8.54817L10.2304 30.4613L32.9403 20.3998L15.6572 -18.6097ZM-7.15244 -8.50365C-9.36225 -7.51103 -19.8876 -2.37917 -20.8693 10.501C-22.0396 25.855 -9.17844 32.0022 -5.87747 33.1862L8.52828 -6.97492C10.5663 -6.24389 22.7842 -0.823122 21.674 13.7436C21.1966 20.0072 18.0974 24.2802 15.9039 26.5039C13.7097 28.7283 11.5371 29.8747 10.3302 30.4168L-7.15244 -8.50365ZM-5.8996 33.1783L-0.0935964 35.2681L14.3564 -4.87714L8.55041 -6.96697L-5.8996 33.1783ZM19.6432 32.4746L33.1293 22.7093L8.10585 -11.8489L-5.38033 -2.08361L19.6432 32.4746ZM33.5935 22.3635C31.818 23.724 29.4422 25.0589 26.4671 25.8373C23.9006 26.5088 18.9444 27.2465 13.3171 24.9419C6.40981 22.1131 -0.114415 14.8039 0.206447 4.70613C0.450069 -2.96084 4.61585 -7.69336 6.08762 -9.20132L36.6217 20.5999C38.3308 18.8488 42.6025 13.9002 42.8516 6.06121C43.1779 -4.20857 36.5588 -11.6459 29.4872 -14.542C23.6956 -16.9138 18.5058 -16.1826 15.6674 -15.44C12.4204 -14.5904 9.7345 -13.1068 7.64172 -11.5031L33.5935 22.3635ZM5.9834 -9.09378L-4.92566 2.24167L25.8169 31.8278L36.726 20.4924L5.9834 -9.09378Z"
                  fill="#FF8718"
                  mask="url(#path-1-inside-1_1840_152)"
                />
              </svg>
            </div>
          </div>
          <span>oris-studio@yandex.ru</span>
        </div>

        <form>
          <fieldset>
            <legend>Написать с сайта</legend>
            <div class="modal__inputs">
              <div class="">
                <label class="sr-only" for="name">Name</label>
                <input
                  class="modal__input"
                  type="text"
                  name="name"
                  id="name"
                  placeholder="Введите ваше имя"
                />
              </div>
              <div class="">
                <label class="sr-only" for="phone">Phone</label>
                <input
                  class="modal__input"
                  type="tel"
                  name="phone"
                  id="phone"
                  placeholder="Введите ваш телефон"
                />
              </div>
            </div>

            <div class="">
              <label class="sr-only" for="comment">Phone</label>
              <textarea
                class="modal__input"
                name="comment"
                id="comment"
                placeholder="Комментарий"
              />
            </div>
          </fieldset>
        </form>
      </div>
      <div class="modal__buttons">
        <TypeButton
          class="modal__button"
          data-modal-hide="modal-form"
          secondary
          color="var(--red)"
          text="Рассчитать проект"
        ></TypeButton>
        <div class="modal__agree">
          <button @click="toggleAgree()">
            <svg
              v-if="!agree"
              width="15"
              height="15"
              viewBox="0 0 15 15"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <rect
                x="0.5"
                y="0.5"
                width="14"
                height="14"
                stroke="var(--main-text)"
              />
            </svg>
            <svg
              v-if="agree"
              width="15"
              height="15"
              viewBox="0 0 15 15"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M5 6.96667L7.56667 9.16667L10.5 5.5"
                stroke="var(--main-text)"
              />
              <rect
                x="0.5"
                y="0.5"
                width="14"
                height="14"
                stroke="var(--main-text)"
              />
            </svg>
          </button>
          <span>Я соглашаюсь с <span>политикой конфиденциальности</span> </span>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup >
import "flowbite";
const agree = ref(false);
function toggleAgree() {
  agree.value = !agree.value;
}
</script>
<style lang="scss">
legend {
  font-size: 18px;
  margin-bottom: 16px;
}
textarea {
  margin-top: 24px;
}
.modal {
  max-width: 618px;
  background-color: var(--bg-card);
  padding: 25px;
  color: var(--main-text);
  &__input {
    background-color: transparent;
    border: none;
    border-bottom: solid 1px var(--grey);
    padding: 0px;
    padding-bottom: 10px;
    width: 100%;
    &::placeholder {
      color: var(--grey);
      font-size: 15px;
      padding-left: 0px;
    }
    &:focus {
      outline: 0;
    }
  }
  &__inputs {
    display: flex;
    justify-content: space-between;
  }
  &__body {
    display: flex;
    flex-direction: column;
    gap: 28px;
    margin: -14px 42px 0px;
  }
  &__title {
    font-size: 33px;
    font-weight: 400;
  }
  &__span {
    font-size: 18px;
    font-weight: 400;
  }
  &__text {
    display: flex;
    flex-direction: column;
    gap: 12px;
  }
  &__icons {
    display: flex;
    gap: 12px;
  }
  &__contact {
    align-items: center;
    display: flex;
    gap: 18px;
  }
  &__info {
    display: flex;
    flex-direction: column;
    gap: 7px;
    font-size: 22px;
    margin-top: 0 !important;
  }
  &__buttons {
    display: flex;
    gap: 40px;
    padding: 30px 42px 35px;
  }
  &__button {
    min-width: 198px;
  }
  &__agree {
    font-size: 12px;
    display: flex;
    align-items: start;
    gap: 10px;
  }
}

@media (max-width: 767px) {
  legend {
    margin-bottom: 10px;
  }
  .modal {
    max-width: 360px;
    &__body {
      margin: 0;
    }
    &__buttons {
      padding: 30px 0px 30px;
      flex-direction: column;
      gap: 12px;
    }
    &__inputs {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
    &__agree {
      gap: 5px;
    }
    &__title {
      font-size: 28px;
      font-weight: 500;
    }
    &__span {
      font-size: 15px;
    }
    &__text {
      gap: 10px;
    }
    &__icons {
      gap: 15px;
    }
    &__contact {
      display: flex;
      gap: 22px;
    }
    &__info {
      font-size: 18px;
    }
  }
  textarea {
    margin-top: 18px;
  }
}
</style>

