<script setup>
import { numbersList } from '@/assets/data'
</script>
<template>
  <button v-for="numbers in numbersList" :key="numbers">{{ numbers }}</button>
</template>
