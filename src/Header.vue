<template>
  <header>
    <img src="/src/assets/logo.png" alt="FLC Logo" />
    <h1>FreeLearnCode</h1>
    <button id="coursesBtn"><h1>All courses ↓</h1></button>
    <button id="profileBtn"><h1>Profile</h1></button>

    <button class="courses" id="course1"><h2>HTML, CSS, JS</h2></button>
    <button class="courses" id="course2"><h2>Python</h2></button>
    <button class="courses" id="course3"><h2>Vue.js</h2></button>
  </header>
</template>

<script setup>
import { onMounted } from 'vue'

onMounted(() => {
  const courses = document.querySelectorAll('.courses')
  const coursesBtn = document.getElementById('coursesBtn')

  // Hide all course buttons initially
  courses.forEach((c) => {
    c.style.display = 'none'
  })

  if (coursesBtn) {
    coursesBtn.addEventListener('click', () => {
      // Use the first course as representative to decide toggle state
      const isVisible = courses.length > 0 && courses[0].style.display !== 'none'
      courses.forEach((course) => {
        course.style.display = isVisible ? 'none' : 'block'
        coursesBtn.querySelector('h1').textContent = isVisible
          ? 'All courses ↓'
          : 'All courses ↑'
      })
    })
  }
})
</script>

<style scoped>
header {
    display: flex;
    background-color: rgb(38, 225, 0);
    height: 60px;
}
header h1, header button {
    align-self: center;
}
header button {
    display: flex;
    background-color: rgb(38, 225, 0);
    height: 60px;
    border-top : none;
    border-bottom : none;
    margin-left: 14px
}
#course1{
    position: absolute;
    top: 68px;
    left: 283px;
    width: 187px;
}
#course2{
    position: absolute;
    top: 125px;
    left: 283px;
    width: 187px;
}
#course3{
    position: absolute;
    top: 183px;
    left: 283px;
    width: 187px;
}
.courses{
    border-top:1px solid black;
}
#coursesBtn:hover{
    cursor: pointer;
    background-color: rgb(25, 148, 0);
}

.courses:hover{
    cursor: pointer;
    background-color: rgb(25, 148, 0);
}
#profileBtn{
    margin-left: 0;
    border-left: none;
}
#profileBtn:hover{
    cursor: pointer;
    background-color: rgb(25, 148, 0);
}
</style>