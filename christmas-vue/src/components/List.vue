<script setup>
import { defineProps, ref, defineEmits } from 'vue'
defineProps(['itemList', 'listTitle'])
const emmits = defineEmits(['moveItemsButtonClicked'])
const moveItem = ref([])
</script>

<template>
  <div>
    <h2>What we {{ listTitle }}</h2>
    <li v-for="(foodItem, index) in itemList" :key="index">
      {{ foodItem.item }} - {{ foodItem.name
      }}<input type="checkbox" :value="foodItem" v-model="moveItem" />
    </li>
    <button @click="emmits('moveItemsButtonClicked', moveItem);moveItem=[]">Move to {{ listTitle }} Item</button>
  </div>
</template>
