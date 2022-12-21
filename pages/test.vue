
<template>
  <div>  <Datepicker class="datePicker" v-model="picked" /> 
  <button @click="check()">check</button></div>

</template>

<script setup>
import Datepicker from 'vue3-datepicker'
import { onMounted, ref } from 'vue';
const picked = ref(new Date())
// console.log("pickers----",picked.value);
// console.log("pickers---- parse",JSON.parse(JSON.stringify(picked.value)) );
// console.log("pickers---- string",JSON.stringify(JSON.parse(picked.value)) );


onMounted(() => {
  console.log('myheader mounted');
});
function check(){

  console.log("pickers---- parse",JSON.parse(JSON.stringify(picked.value)) );
// console.log("pickers----",picked);
}
</script>



<!-- date pickers
https://icehaunter.github.io/vue3-datepicker/
https://www.npmjs.com/package/vue3-datepicker


https://icehaunter.github.io/vue3-datepicker/examples.html-->


<style scoped>
.datePicker{
  border: 2px solid red;
}
</style>