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
            <button id="courseA" class="courses"><h1>HTML, CSS, JS</h1></button>
            <button id="courseB" class="courses"><h1>Python</h1></button>
            <button id="courseC" class="courses"><h1>Vue.js</h1></button>
            <button id="courseD" class="courses"><h1>Lua</h1></button>
        </main>
    </body>
</template>

<style scoped>
.courses{
   padding: 5px;
   margin: 30px;
   font-size: 40px;
   border-radius: 50px;
   background-color: rgb(122, 255, 248);
   transition: 0.5s ease-in-out;
   transition: transform 0.3s ease, box-shadow 0.3s ease;
  box-shadow: 0 6px 20px rgba(0, 168, 159, 0.3);
 }
.courses:hover{
   padding: 20px;
   font-size: 42px;
   border-radius: 50px;
   background-color: rgb(0, 168, 159);
   transform: scale(1.07);
   box-shadow: 0 12px 25px rgba(0, 168, 159, 0.45);
 }

</style>
