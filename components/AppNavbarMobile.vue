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
  padding: 5px 10%;
  width: -webkit-fill-available;
}
@media screen and (max-width: 900px) {
  .nav_mobile{
    display: flex;
  }
  .nav_mobile img  {
    width: 100px;
  }
}
</style>
