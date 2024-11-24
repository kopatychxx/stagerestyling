<script setup>

</script>

<template>
    <div class="landing_page">
      <div class="mainText">
        <h1 class="mainText_header">Choose your stage,<br>define your <span class="header_highlight">style!</span></h1>
        <a href="" class="button"><p>Ask for a price</p>
            <img src="../static/arrow.svg" alt="">
          </a>
      </div>
    </div>
</template>

<script>
export default {
  name: "LandingPage",
}
</script>

<style scoped>
.landing_page{
  background-image: url(../static/bg.png);
  height: 100vh;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  margin-top: auto;
  align-content: center;
  padding-left: 180px;
}
.mainText_header{
  font-family: 'Quicksand', sans-serif !important;
  font-size:48px;
  font-weight: 400;
  text-align:left;
  vertical-align:text-top;
  color: white;
}
.header_highlight{
  color: #9F0000;
}
.button {
  display: flex;
  justify-content: space-between;
  width: 190px;
  margin-top: 30px;
  text-decoration: 1px solid;
  font-size: 20px;
  color: white;
  border-bottom: 2px solid white;
}
.button:hover:before {
  left: 7px;
}
@keyframes bounce {
  0%, 20%, 60%, 100% {
    transform: translateY(0);
  }

  40% {
    transform: translateY(-20px);
  }

  80% {
    transform: translateY(-10px);
  }
}
.button:hover {
  animation: bounce 1s;
}
.btn_price p {
  font-size: 20px;
  font-weight: 300;
  color: white;
}
@media screen and (max-width: 900px) {
  .landing_page{
    padding-left: 0;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
  }
  .mainText_header{
    font-size: 40px;
    text-align: center;
  }
  .mainText{
    justify-items: center;
  }
  .button {
    display: flex;
    margin: 35px auto;
  }
}
@media screen and (max-width:600px) {

}
</style>
