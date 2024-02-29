<template>
  <div class="card" :style="{ background: bgColor, color: color }">
    <p class="card__text">{{ paragraph }}</p>
    <div class="card__block">
      <span class="card__action">{{ span }}</span>
      <TypeButton
        data-modal-target="modal-form"
        data-modal-toggle="modal-form"
        primary
        color="var(--red)"
        text="Связаться"
      />
      <ModalForm></ModalForm>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.card {
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  gap: 10px;
  padding: 30px 15px;
  &__block {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }
}
@media (min-width: 768px) {
  .card {
    padding: 30px 50px;
    &__block {
      flex-direction: row;
      gap: 30px;
    }
    &__text {
      max-width: 585px;
    }
  }
}
@media (min-width: 1440px) {
  .card {
    gap: 30px;
    padding: 30px 60px;
    &__text {
      max-width: 660px;
    }
  }
}
</style>
<script setup lang="ts">
const props = defineProps<{
  bgColor: string;
  color: string;
  span: string;
  paragraph: string;
}>();
</script>
    