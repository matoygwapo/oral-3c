<template>
    <div class="child">
        <h2>This is from child component</h2>
        <p>{{ props.message }}</p>
        <input type="text" placeholder="Change message">
        <button @click="callFunctionFromParent">Click Me</button>
        <AnotherComponent/>
    </div>
</template>

<script setup>
import AnotherComponent from './AnotherComponent.vue';
const props = defineProps(['message','callBack'])

//change the message value based on user input in this child component
const callFunctionFromParent = ()=>{
    props.callBack();
    //Hello from child
}
</script>

<style scoped>
h1,h2{
    color:red;
}
.child{
    border:1px solid;
    padding:10px;
}

</style>