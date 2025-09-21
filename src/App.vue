

<template>
  <div>
    <h1>{{ people.name }}</h1>
    <h1>{{ people.age }}</h1>
    <h1>{{ re }}</h1>
  </div>
  <br>

<div>
  <input v-model="people.name">
  <input type="button" @click="changeAge" value="改变年龄">
</div>
</template>

<script setup>
import { computed, ref,watch } from 'vue'
const people=ref({name:'张三',age:20})
function changeAge(){
  people.value.age+=1
}
let re=computed({
  get(){
     return people.value.name+'age is'+people.value.age

  }
  ,set(value){
    console.log('set得到的'+value)
  }
 
   
 
})
let stop=watch(people,(newValue,oldValue)=>{
  console.log(newValue,oldValue)
  if(newValue.age>30){
    stop()
  }

},{deep:true})


</script>



