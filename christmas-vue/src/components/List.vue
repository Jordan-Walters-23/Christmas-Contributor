<script setup>
import { defineProps, ref } from 'vue'
defineProps(['itemList', 'listTitle'])
const moveItem = ref([])
</script>

<template>
  <div>
    <button @click="">Move to have Item</button>
    <h2>What we {{ listTitle }}</h2>
    <li v-for="(foodItem, index) in itemList" :key="index">
      {{ foodItem.item }} - {{ foodItem.name
      }}<input type="checkbox" :value="foodItem" v-model="moveItem" />
    </li>
  </div>
</template>
