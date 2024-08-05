<script setup>
import { numbersList } from '@/assets/data'

const emit = defineEmits(['convert'])
</script>
<template>
  <div>
    <button v-for="numbers in numbersList" :key="numbers" @click="$emit('convert', numbers)">
      {{ numbers }} km
    </button>
  </div>
</template>
<style scoped>
button {
  margin: 0 30px;
  padding: 15px 20px;
  border: none;
  background-color: #b464e8;
  border-radius: 5px;
}
</style>
