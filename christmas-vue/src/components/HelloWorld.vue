<script setup>
import { ref } from 'vue'
import List from './List.vue'
const have = ref([
  {
    item: 'turkey',
    name: 'Matt'
  },

  { item: 'carrots', name: 'Jordan' }
])
const need = ref([{ item: 'gravy', name: 'Matt'}, { item: 'gravy', name: 'Matt'}])
const message = ref('')
const name = ref('')
function addToHaveArray() {
  console.log(have)
  console.log(have.value)
  have.value.push({ item: message.value, name: name.value })
  message.value = ''
  name.value = ''
}
</script>

<template>
  <h1>Christmas Dinner!</h1>
  <List :itemList="have" listTitle="have"/>
  <List :itemList="need" listTitle="need"/>
  <div>
    <input v-model="message" placeholder="Add Item..." />
    <input v-model="name" placeholder="Your Name.." />
    <button @click="addToHaveArray">Add Item</button>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
