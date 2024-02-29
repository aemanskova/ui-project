<template>
  <span :style="{ color: textColor, fontSize: 'inherit' }">
    <slot></slot>
  </span>
</template>

<script setup lang="ts">
defineProps(["textColor"]);
</script>
