<template>7°</template>
<script setup>
import { useWeather } from '@/composables/useWeather'
import { onMounted } from 'vue'

onMounted(() => {
  useWeather()
})
</script>
<style scoped></style>
