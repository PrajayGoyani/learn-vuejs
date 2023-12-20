<template>
    <h1>{{ title }}</h1>
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <input type="text" ref="name" />
    <button @click="handleClick">click me</button>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import { ref } from 'vue';

const text = ref();

export default {
    name: 'App',
    components: {
        HelloWorld
    },
    data() {
        return {
            title: "My First Vue App :)"
        }
    },
    methods: {
        handleClick() {
            console.log(this.$refs.name.value);
        }
    }
}
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 100px;
}
h1 {
    border-bottom: 1px solid #ddd;
    display: block;
    padding: 10px;
    background-color: #2c3e50;
    color: white;
}
</style>
