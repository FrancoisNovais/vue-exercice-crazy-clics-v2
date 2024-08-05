<script setup>
import { wordsList } from '@/assets/data'

const emit = defineEmits(['correctedWord'])
</script>
<template>
  <div>
    <button v-for="word in wordsList" :key="word" @click="$emit('correctedWord', word)">
      {{ word }}
    </button>
  </div>
</template>
<style scoped>
button {
  margin: 0 20px;
  padding: 15px 20px;
  border: none;
  background-color: #61e6b7;
  border-radius: 5px;
}
</style>
