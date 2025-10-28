<script setup>
import Header from './Header.vue';
</script>

<template>
    <Header />
    <body>
        <h1>Welcome to FreeLearnCode!</h1>
        <H1>Your gateway to free coding education.</H1>
        <h1>I love to let users learn to code for free!</h1>
        <h1>Pick any cource below:</h1>
        <main>
            <button id="courseA"><h1>HTML, CSS, JS</h1></button>
            <button id="courseB"><h1>Python</h1></button>
            <button id="courseC"><h1>Vue.js</h1></button>
        </main>
    </body>
</template>

<style scoped>
 #courseA, #courseB, #courseC{
    position: absolute;
    top: 320px;
    width: 400px;
    height: 400px;
    font-size: 40px;
    border-radius: 50px;
    background-color: rgb(122, 255, 248);
    transition: 0.5s ease-in-out;
 }
 #courseA:hover, #courseB:hover, #courseC:hover{
    position: absolute;
    top: 310px;
    width: 415px;
    height: 415px;
    font-size: 42px;
    border-radius: 50px;
    background-color: rgb(0, 168, 159);
 }
 #courseB{
    left: 500px
 }

 #courseC{
    left: 980px
 }
</style>
