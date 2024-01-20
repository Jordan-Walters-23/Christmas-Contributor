<script setup>
  import {ref} from 'vue' 
  const have = ref([{item: 'turkey'}, {item: 'carrots'}])
  const need = ref([{item: 'gravy' }])

</script>

<template>
  <h1>Christmas Dinner! </h1>
  <div>
    <h2>What we have</h2>
    <li v-for="item in have">{{ item  }}</li>
  </div>
  <div>
    <h2>What we need</h2>
    <li v-for="item in need">{{  item }}</li>
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
