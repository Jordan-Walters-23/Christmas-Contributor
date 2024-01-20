<script setup>
  import {ref} from 'vue'
  import List from './List.vue'
  const have = ref([{item: 'turkey'}, {item: 'carrots'}])
  const need = ref([{item: 'gravy' }])
  const message = ref('')
  function addToHaveArray() { 
    console.log(have)
    console.log(have.value)
    have.value.push({item: message.value})
    message.value= ""
  }
</script>

<template>
  <h1>Christmas Dinner! </h1>
  <List :itemList="have"/>
  <List :itemList="need"/>
  <div>
    <input v-model="message" placeholder="Add Item..." />
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
