<script setup xmlns:active="http://www.w3.org/1999/xhtml">

</script>

<template>
  <div>
    <div class="hamburger-menu" @click="toggleMenu">
      <div class="hamburger" :class="{ active: isActive }">
        <span></span>
        <span></span>
        <span></span>
      </div>
    </div>
    <div class="menu" :class="{ active: isActive }">
      <a href="#" @click="toggleMenu" @click.prevent="scrollToSection('home')">Home</a>
      <a href="#" @click="toggleMenu" @click.prevent="scrollToSection('about')">About us</a>
      <a href="#" @click="toggleMenu" @click.prevent="scrollToSection('service')">Service</a>
      <a href="#" @click="toggleMenu" @click.prevent="scrollToSection('portfolio')">Portfolio</a>
      <a href="#" @click="toggleMenu" @click.prevent="scrollToSection('contact')">Contact</a>

    </div>
  </div>
</template>

<script>
export default {
  name: "HamburgerMenu",
  data() {
    return {
      isActive: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isActive = !this.isActive;
    },
    scrollToSection(sectionId) {
      const element = document.getElementById(sectionId);
      if (element) {
        this.$scrollTo(element, { offset: -50, duration: 1000 });
      }
    }
  },
};
</script>

<style scoped>

.hamburger-menu {
  display: flex;
  justify-content: flex-end;
  padding: 20px;
  position: relative;
}
.hamburger {
  width: 30px;
  height: 25px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  cursor: pointer;
  z-index: 2;
  transition: transform 0.3s ease;
}
.hamburger span {
  display: block;
  height: 3px;
  width: 30px;
  background-color: #9f0000;
  border-radius: 5px;
  transition: all 0.3s ease;
}
.menu {
  position: fixed;
  top: 0;
  left: 0;
  height: 100vh;
  width: 100vw;
  background-color: rgba(0, 0, 0, 0.7);
  color: white;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  transform: translateX(-100%); /* Меню скрыто по умолчанию */
  transition: transform 0.3s ease;
  z-index: 1;
}
.menu a {
  color: white;
  text-decoration: none;
  font-size: 24px;
  margin: 20px 0;
  transition: color 0.3s ease;
}
.menu a:hover {
  color: #ff6347; /* Цвет при наведении */
}
.hamburger.active span:nth-child(1) {
  transform: rotate(45deg); /* Верхняя линия превращается в верхнюю часть крестика */
  position: relative;
  top: 10px;
}
.hamburger.active span:nth-child(2) {
  opacity: 0; /* Средняя линия исчезает */
}
.hamburger.active span:nth-child(3) {
  transform: rotate(-45deg); /* Нижняя линия превращается в нижнюю часть крестика */
  position: relative;
  top: -10px;
}
.menu.active {
  transform: translateX(0); /* Показываем меню */
}
</style>
