<template>
  <div class="column">
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
 div.column {
   display: flex;
   flex-direction: column;

   justify-content: v-bind(mainAxis);
   align-items: v-bind(crossAxis);
 }
</style>