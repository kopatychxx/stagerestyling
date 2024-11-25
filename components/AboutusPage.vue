<script setup>

</script>

<template>
  <div id="about" class="aboutus" >
    <img class="aboutus_img" src="../static/abuoutus.png" alt="">
    <div class="aboutus_info">
      <h3 class="aboutus_info_header">About us</h3>
      <p class="aboutus_info_text">
        At <span> Stage Restyling</span>, we specialize in high-quality vehicle wraps and protective films. Our team offers custom solutions that not only enhance your car’s appearance but also protect it from the elements. Using top-grade materials, we ensure long-lasting results and customer satisfaction
        <br><br>
        We are committed to delivering the best service, from consultation to installation, to bring your vision to life and give your vehicle a unique look.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "AboutusPage",
}
</script>

<style scoped>
.aboutus {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin: 75px 0;
  align-items: center;
}
.aboutus_info {
  display: flex;
  flex-direction: column;
  align-items: end;
  margin-right: 10%;
  width:40%;
}
.aboutus_img {
  width: 40%;
  height: 100%;
}
.aboutus_info_header{
  font-size: 48px;
  text-align: left;
  font-family: 'Quicksand', sans-serif !important;
  font-weight: 300;
}
.aboutus_info_text{
  font-size: 24px;
  font-weight: 300;
  text-align: right;
  margin-top: 36px;
}
.aboutus_info_text span  {
  color: #9F0000;
  font-weight: 400;
}
@media screen and (max-width: 900px) {
  .aboutus {
    flex-direction: column-reverse;
    align-items: start;
  }
  .aboutus_info_header {
    font-size: 30px;
  }
  .aboutus_info {
    display: flex;
    margin: 0 auto 50px;
    align-items: center;
    width: 80%;
  }
  .aboutus_info_text {
    text-align: center;
    font-size: 20px;
  }
  .aboutus_img {
    width: 70%;
  }
}
</style>
