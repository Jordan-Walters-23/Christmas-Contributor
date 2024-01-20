<script setup>
  import {defineProps} from 'vue'
  defineProps(["itemList"])
</script>

<template>
<div>
    <h2>What we have</h2>
    <li v-for="(foodItem, index) in itemList" :key=index>{{ foodItem.item }} - {{ foodItem.name  }}</li>
  </div>
</template>