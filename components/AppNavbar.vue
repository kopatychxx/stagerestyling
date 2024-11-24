<script setup>
</script>

<template>
  <div class="header">
    <div class="logo_stage_Restyling"><img src="../static/logo_stage_restyling.png" alt="logo_stage_Restyling"></div>
    <div class="nav">
      <a href="/stageRestyling/pages">Home</a>
      <a href="/">About us</a>
      <a href="">Service</a>
      <a href="">Portfolio</a>
      <a href="">Contact</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppNavbar"
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
}
.nav a {
  margin-right: 38px;
  text-decoration: none;
  color: white;
  font-family: 'Quicksand', sans-serif;
}
.nav a li:last-child {
  margin: 0;
}
a {
  position: relative;
  color: WHITE;
  cursor: pointer;
  line-height: 1;
  text-decoration: none;

}
a:after {
  display: block;
  position: absolute;
  left: 0; /*изменить на right:0;, чтобы изменить направление подчёркивания */
  width: 0;/*задаём длинну линии до наведения курсора*/
  height: 2px; /*задаём ширину линии*/
  background-color: white; /*задаём цвет линии*/
  content: "";
  transition: width 0.5s ease-out; /*задаём время анимации*/
}
a:hover:after,
a:focus:after {
  width: 100%; /*устанавливаем значение 100% чтобы ссылка подчёркивалась полностью*/
}
@media screen and (max-width: 900px) {
  .header {
    display: none;
  }
}
</style>
