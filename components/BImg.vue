<script setup lang="ts">
import { computed } from 'vue'
import b from './b.png'

const style = computed(() => ({
  backgroundImage: `url(${b})`,
  width: '100px',
  height: '100px',
}))
</script>

<template>
  <div :style="style" />
</template>
