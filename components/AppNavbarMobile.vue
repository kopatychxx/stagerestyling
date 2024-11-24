<script setup>

</script>

<template>
  <div class="nav_mobile">
    <img src="../static/logo_stage_restyling.png" alt="">
    <HamburgerMenu/>
  </div>
</template>

<script>
export default {
  name: "AppNavbarMobile",
}
</script>
<style scoped>
.nav_mobile {
  position: fixed;
  display: none;
  justify-content: space-between;
  align-items: center;
  margin: auto 10%;
  padding: 20px 0;
  width: -webkit-fill-available;
}
.nav {
  display: flex;
  flex-direction: column;
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
.nav_mobile_btn {
  color: #ffffff;
  cursor: pointer;
}
@media screen and (max-width: 900px) {
  .nav_mobile{
    display: flex;
  }
}
</style>
