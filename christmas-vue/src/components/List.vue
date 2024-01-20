<script setup>
  import {defineProps} from 'vue'
  defineProps(["itemList", "listTitle"])
</script>

<template>
<div>
    <h2>What we {{ listTitle }} </h2>
    <li v-for="(foodItem, index) in itemList" :key=index>{{ foodItem.item }} - {{ foodItem.name  }}</li>
  </div>
</template>