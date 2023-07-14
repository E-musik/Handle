<script setup>
import { ref } from 'vue'

const greet = ref ('HELLO WORLD!')
function reversegreet() {
  greet.value = greet.value.split('').reverse().join('')
}
function notify() {
  alert('Accesseed Granted')
}
</script>

<template>
  <h1>{{ greet }}</h1><br>

  <button @click="reversegreet"> Mirro message</button> <br>

  <button @click="greet+= '!'">Append "!"</button>

  <br><a href="https://vuejs.org" @click.prevent="notify">Link to Access</a>

</template>

<style scoped>

button{
 display: block;
 margin-bottom: 2em; 
 border-radius: 10px;
 background-color: greenyellow;

}
h1{
  color: lime;
  display: inline-block;
  font-size: 40px;
}
</style>
