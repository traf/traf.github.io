<template>
  <AppHeader
    :style="{
      borderColor: y > 10 ? 'var(--border-color)' : 'transparent'
    }"
  />
</template>

<script setup>
import { useWindowScroll } from '@vueuse/core'

const { y } = useWindowScroll()
</script>

<style>
  .app-header {
    position: sticky;
    top: 0;
    z-index: 100;
    background: var(--background-semi);
    backdrop-filter: var(--blur);
    padding: var(--ui-padding-y) var(--ui-padding-x) !important;

    border-bottom: var(--border);
    border-color: transparent;
    transition: border-color var(--speed);
  }
</style>
