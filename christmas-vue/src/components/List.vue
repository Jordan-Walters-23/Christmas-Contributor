<script setup>
  import {defineProps} from 'vue'
  defineProps(["itemList"])
</script>

<template>
<div>
    <h2>What we have</h2>
    <li v-for="(item, index) in itemList" :key=index>{{ item.item }}</li>
  </div>
</template>