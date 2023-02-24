<script setup lang="ts">
import { computed } from 'vue'
import a from './a.png'

const style = computed(() => ({
  backgroundImage: `url(${a})`,
  width: '100px',
  height: '100px',
}))
</script>

<template>
  <div :style="style" />
</template>
