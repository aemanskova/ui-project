

<template>
  <div class="container">
    <nav class="navbar">
      <svg
        width="30"
        height="30"
        viewBox="0 0 30 30"
        fill="currentColor"
        xmlns="http://www.w3.org/2000/svg"
      >
        <circle cx="15" cy="15" r="15" fill="#F94747" />
      </svg>
      <ul class="navbar__list">
        <li>Услуги</li>
        <li>Кейсы</li>
        <li>Решения для бизнеса</li>
        <li>Контакты</li>
        <li>
          <button
            id="dropdownMenuIconHorizontalButton"
            data-dropdown-toggle="dropdownDotsHorizontal"
          >
            <svg
              width="28"
              height="9"
              viewBox="0 0 28 9"
              fill="#F94747"
              xmlns="http://www.w3.org/2000/svg"
            >
              <circle cx="24.4193" cy="4.49985" r="3.5814" />
              <circle cx="14.0014" cy="4.49985" r="3.5814" />
              <circle cx="3.58145" cy="4.49985" r="3.5814" />
            </svg>
          </button>
          <DropDownMenu
            id="dropdownDotsHorizontal"
            buttonId="dropdownMenuIconHorizontalButton"
            :items="arrayMenu"
          ></DropDownMenu>
        </li>
      </ul>
      <div class="navbar__box">
        <TypeButton
          data-modal-target="modal-form"
          data-modal-toggle="modal-form"
          primary
          color="var(--purple)"
          text="Связаться"
        />
        <!-- <button  @click="changeTheme">theme</button> -->
        <SwitchTheme class="navbar__switch" @switched="changeTheme" />
        <ModalForm></ModalForm>
        <button
          id="dropdownMenuIconHorizontalButtonMobile"
          data-dropdown-toggle="dropdownDotsHorizontalMobile"
          class="navbar__points"
        >
          <svg
            width="28"
            height="9"
            viewBox="0 0 28 9"
            fill="#F94747"
            xmlns="http://www.w3.org/2000/svg"
          >
            <circle cx="24.4193" cy="4.49985" r="3.5814" />
            <circle cx="14.0014" cy="4.49985" r="3.5814" />
            <circle cx="3.58145" cy="4.49985" r="3.5814" />
          </svg>
        </button>
        <DropDownMenu
          id="dropdownDotsHorizontalMobile"
          buttonId="dropdownMenuIconHorizontalButtonMobile"
          :items="arrayMenuMobile"
        ></DropDownMenu>
      </div>
    </nav>
    <span style="color: var(--main-text)">Создай свой бренд / вакансии</span>
  </div>
</template>
<script setup>
const arrayMenu = ["Пункт 1", "Пункт 2", "Пункт 3", "Пункт 4"];
const arrayMenuMobile = ["Услуги", "Кейсы", "Решения для бизнеса", "Контакты"];
</script>
<style lang="scss" scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  &__list {
    display: none;
    gap: 50px;
    color: var(--main-text);
    list-style-type: none;
  }
  &__box {
    display: flex;
    justify-content: space-around;
    align-items: center;
    gap: 20px;
  }
}
.container {
  display: flex;
  overflow: hidden;
  flex-direction: column;
  gap: 24px;
}
@media (min-width: 768px) {
  .navbar {
    &__box {
      gap: 50px;
    }
    &__switch {
      order: -2;
    }
  }
  .container {
    gap: 22px;
  }
}

@media (min-width: 1440px) {
  .navbar {
    &__list {
      display: flex;
      align-items: center;
    }
    &__points {
      display: none;
    }
  }
  .container {
    gap: 16px;
  }
}
</style>
<script>
export default {
  methods: {
    changeTheme() {
      const htmlElement = document.documentElement;
      if (htmlElement.classList.contains("dark-mode")) {
        htmlElement.classList.remove("dark-mode");
        htmlElement.classList.add("light-mode");
      } else {
        htmlElement.classList.remove("light-mode");
        htmlElement.classList.add("dark-mode");
      }
    },
  },
};
</script>