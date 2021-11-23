<template>
  <div class="row">
    <slot/>
  </div>
</template>

<script lang="ts" setup>
 import {defineProps} from 'vue'

 const props = defineProps({
   mainAxis: {
     type: String,
     default: "flex-start"
   },

   crossAxis: {
     type: String,
     default: "flex-start"
   }
 })
</script>

<style scoped>
 div.row {
   display: flex;
   flex-direction: row;

   justify-content: v-bind(mainAxis);
   align-items: v-bind(crossAxis);
 }
</style>