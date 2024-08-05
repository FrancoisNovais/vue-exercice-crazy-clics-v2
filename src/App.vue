<script setup>
import PartOne from './components/PartOne.vue'
import PartTwo from './components/PartTwo.vue'
import PartThree from './components/PartThree.vue'

import { ref } from 'vue'
const result = ref('')

// Part One
const correctedWord = (word) => {
  const firstLetter = word[0].toUpperCase()
  const otherLetters = word.slice(1).toLowerCase()
  result.value = firstLetter + otherLetters
}

// Part Two
import { colorsList } from '@/assets/data'

const randomColor = () => {
  const randomIndex = Math.floor(Math.random() * colorsList.length)
  result.value = colorsList[randomIndex]
}

// Part Three
const convert = (numbers) => {
  result.value = `${numbers} km = ${numbers * 100000} cm.`
}
</script>

<template>
  <main>
    <h1>Crazy clics v2</h1>
    <div>
      <div class="buttons">
        <PartOne @correctedWord="correctedWord" />
        <PartTwo @randomColor="randomColor" />
        <PartThree @convert="convert" />
      </div>
      <div class="result">
        <h2>Le résultat</h2>
        <div>
          <p>{{ result }}</p>
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped>
main {
  display: flex;
  flex-direction: column;
  align-items: center;
  height: 100vh;
  gap: 100px;
}
main > div {
  display: flex;
  gap: 100px;
  justify-content: space-evenly;
}
.buttons {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 100px;
}
.result {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 30px;
}
.result > div {
  width: 200px;
  height: 30px;
  border: 2px solid grey;
  display: flex;
  align-items: center;
  justify-content: center;
}

h1 {
  font-size: 48px;
  font-weight: bold;
  margin-top: 30px;
}

h2 {
  font-size: 24px;
  font-weight: bold;
}
</style>
