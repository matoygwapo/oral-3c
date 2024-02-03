<template>
  <div>
    <h1>Greetings from root component</h1>
    <ChildComponent :message="message" :callBack="functionFromParent"/>
  </div>
</template>

<script setup>
import ChildComponent from './components/ChildComponent.vue'
import {ref} from 'vue'

const message = ref("This is a message from parent")

const functionFromParent = ()=>{
  // alert("This is a function from parent")
  //change the message value to another string
}

</script>

<style>
h1,h2{
  opacity: 0.5;
}
</style>