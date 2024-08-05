<script setup>
import { wordsList } from '@/assets/data'
</script>
<template>
  <div>
    <button v-for="word in wordsList" :key="word">
      {{ word }}
    </button>
  </div>
</template>
