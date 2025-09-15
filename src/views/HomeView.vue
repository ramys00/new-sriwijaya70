<script setup>
import { ref, onMounted, onUnmounted } from "vue";
import Navbar from "../components/Navbar.vue";

const scrollY = ref(0);

const handleScroll = () => {
  scrollY.value = window.scrollY;
};

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});
</script>

<template>
  <div class="page-container">
    <Navbar />
    <div class="intro-container">
      <div class="sprite-container">
        <img src="/src/assets/sprite/az.png" alt="az" class="sprite-image" />
        <img
          src="/src/assets/sprite/cassie.png"
          alt="cassie"
          class="sprite-image"
        />
      </div>
      <img
        src="/src/assets/hourlies_logo2.png"
        alt="Hourlies Logo"
        class="hourlies-logo"
      />
    </div>
    <div class="about-container">
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsam earum,
        exercitationem dolorum quibusdam est deserunt, sequi suscipit minima
        saepe iste a itaque nobis voluptatem quae repellendus dicta, rem sed
        illo.
      </p>
    </div>
  </div>
</template>
<style scoped>
.page-container {
  height: 1000px;
  background-image: linear-gradient(rgb(73, 70, 104), rgb(30, 29, 43));
}
.intro-container {
  display: flex;
  flex-direction: column;
  margin-top: 75px;
  position: relative;
}
.sprite-container {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-evenly;
}
.about-container {
  height: 350px;
  background-color: rgb(30, 29, 43);
}
.hourlies-logo {
  width: 350px;
  align-self: center;
  position: absolute;
  top: 100px;
  z-index: 0;
}
.sprite-image {
  height: 500px;
}
</style>
