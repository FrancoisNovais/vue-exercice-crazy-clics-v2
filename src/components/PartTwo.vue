<script setup>
const emit = defineEmits(['randomColor'])
</script>
<template>
  <div>
    <button @click="$emit('randomColor')">Couleur surprise</button>
  </div>
</template>
<style scoped>
button {
  margin: 0 30px;
  padding: 15px 25px;
  border: 2px solid #5ec2da;
  border-radius: 50px;
  background-color: white;
  color: #5ec2da;
  font-size: 20px;
}
</style>
