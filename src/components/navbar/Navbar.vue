<template>
  <div class="navbar__wrapper">
    <nav class="navbar">
      <div class="navbar__buttons__row">
        <button>(21) 2042-4442</button>
        <button>TOUR VIRTUAL</button>
        <button>WHATSAPP</button>
      </div>
      <div class="navbar__select__car__row">
        <p v-for="index in 8" :key="index">{{ index }}</p>
        <p>X</p>
        <p>Z</p>
        <p>M</p>
        <p>I</p>
        <p>Plug-in-Hybrid</p>
      </div>
    </nav>
    <CarsSlide />
  </div>
</template>

<script>
import "./Navbar.css";
import CarsSlide from "../carsSlide/CarsSlide.vue";
export default {
  name: "Navbar",
  components: {
    CarsSlide,
  },
};
</script>
