<script setup>
import Datepicker from 'vue3-datepicker'
import { ref } from 'vue'
const picked = ref(new Date())
</script>

<template>
  <Datepicker class="datePicker" v-model="picked" />
</template>



<!-- date pickers
https://icehaunter.github.io/vue3-datepicker/
https://www.npmjs.com/package/vue3-datepicker


https://icehaunter.github.io/vue3-datepicker/examples.html-->


<style scoped>
.datePicker {
 
  "--vdp-bg-color": "#ea5d5d",
  "--vdp-text-color": "#000000",
  "--vdp-box-shadow": "0 4px 10px 0 rgba(128, 144, 160, 0.1), 0 0 1px 0 rgba(128, 144, 160, 0.81)",
  "--vdp-border-radius": "5px",
  "--vdp-heading-size": "2.5em",
  "--vdp-heading-weight": "bold",
  "--vdp-heading-hover-color": "#eeeeee",
  "--vdp-arrow-color": "#000000",
  "--vdp-elem-color": "#854242",
  "--vdp-disabled-color": "#d5d9e0",
  "--vdp-hover-color": "#ffffff",
  "--vdp-hover-bg-color": "#0baf74",
  "--vdp-selected-color": "#ffffff",
  "--vdp-selected-bg-color": "#0baf74",
  "--vdp-current-date-outline-color": "#888888",
  "--vdp-current-date-font-weight": "bold",
  "--vdp-elem-font-size": "0.8em",
  "--vdp-elem-border-radius": "5px",
  "--vdp-divider-color": "#8cbb8b"
}
</style>