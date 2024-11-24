<script setup>
</script>

<template>
  <div class="header">
    <div class="logo_stage_Restyling"><img src="../static/logo_stage_restyling.png" alt="logo_stage_Restyling"></div>
      <ul class="nav">
        <li class="nav_button" @click="scrollToSection('home')">Home</li>
        <li class="nav_button" @click="scrollToSection('about')">About us</li>
        <li class="nav_button">Service</li>
        <li class="nav_button">Portfolio</li>
        <li class="nav_button">Contact</li>
      </ul>
  </div>
</template>

<script>
import VueScrollTo from 'vue-scrollto'
export default {
  name: "AppNavbar",
    methods: {
      scrollToSection() {
        VueScrollTo.scrollTo('#about', 900)  // Прокрутка к элементу с id="about" за 800 мс
      },
    }
}
</script>

<style scoped>
.header {
  position: fixed;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: auto 10%;
  padding: 20px 0;
  width: -webkit-fill-available;
}
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: rgba(217, 217, 217, 0.2);
  padding: 14px 20px;
  border-radius: 20px;
  list-style: none;
}
.nav ul li {
  text-decoration: none;
  color: white;
  font-family: 'Quicksand', sans-serif;
}
.nav_button {
  margin-right: 20px;
}
.nav ul li:last-child {
  margin: 0;
}
li {
  position: relative;
  color: WHITE;
  cursor: pointer;
  line-height: 1;
  text-decoration: none;

}
li:after {
  display: block;
  position: absolute;
  left: 0; /*изменить на right:0;, чтобы изменить направление подчёркивания */
  width: 0;/*задаём длинну линии до наведения курсора*/
  height: 2px; /*задаём ширину линии*/
  background-color: white; /*задаём цвет линии*/
  content: "";
  transition: width 0.5s ease-out; /*задаём время анимации*/
}
li:hover:after,
li:focus:after {
  width: 100%; /*устанавливаем значение 100% чтобы ссылка подчёркивалась полностью*/
}
@media screen and (max-width: 900px) {
  .header {
    display: none;
  }
}
</style>
