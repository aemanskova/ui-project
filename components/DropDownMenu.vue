<template>
  <div
    :id="id"
    class="dropdown z-10 hidden divide-y divide-gray-100 rounded-lg shadow w-44"
  >
    <ul class="py-2 text-sm" :aria-labelledby="buttonId">
      <li v-for="item in items" :key="item.index">
        <a href="#" class="block px-4 py-2">{{ item }}</a>
      </li>
    </ul>
  </div>
</template>
<script setup>
import "flowbite";

const props = defineProps({
  id: { type: String, default: "default-modal" },
  buttonId: { type: String, default: "default-modal-button" },
  items: Array,
});
</script>
<style>
.dropdown {
  background-color: var(--bg-card);
  color: var(--main-text);
}
@media (max-width: 766px) {
  .dropdown {
    overflow: hidden;
    /* max-width: 100px !important; */
    width: 70vw !important;
  }
}
</style>