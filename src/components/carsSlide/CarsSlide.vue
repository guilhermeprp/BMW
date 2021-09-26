<template>
  <div class="cars__slide">
    <div class="cars__slide__container">
      <div class="cars__slide__wrappper">
        <button class="cars__slide__arrow__left" @click="scrollLeft">
          &lt;
        </button>
        <div
          class="cars__slide__wrappper__container"
          v-for="item in 3"
          :key="item"
        >
          <CarCard v-for="item in 4" :key="item" />
        </div>
        <button class="cars__slide__arrow__right" @click="scrollRight">
          &gt;
        </button>
      </div>
      <div class="cars__slide__control__buttons">
        <button
          :class="{ clicked: selectedButton.buttonA }"
          @click="scrollToStart()"
        ></button>
        <button
          :class="{ clicked: selectedButton.buttonB }"
          @click="scrollToMiddle()"
        ></button>
        <button
          :class="{ clicked: selectedButton.buttonC }"
          @click="scrollToEnd()"
        ></button>
      </div>
    </div>
  </div>
</template>

<script>
import CarCard from "../body/subcomponents/carCard/CarCard.vue";
import "./CarsSlide.css";
export default {
  name: "CarsSlide",
  components: {
    CarCard,
  },
  data() {
    return {
      slideBox: Element,
      slideWidth: Number,
      selectedButton: [{ buttonA: true, buttonB: false, buttonC: false }],
    };
  },
  mounted() {
    this.slideBox = document.querySelector(".cars__slide__wrappper");
    this.slideWidth = this.slideBox.scrollWidth;
  },
  methods: {
    scrollRight() {
      this.slideBox.scrollBy(1000, 0);
    },
    scrollLeft() {
      this.slideBox.scrollBy(-1000, 0);
    },
    scrollToStart() {
      this.slideBox.scrollBy(-this.slideWidth, 0);
    },
    scrollToMiddle() {
      var slideValue = this.slideWidth * 0.3;
      if (this.slideBox.scrollLeft < 60) {
        this.slideBox.scrollBy(slideValue, 0);
      }
      if (this.slideBox.scrollLeft > 2900) {
        this.slideBox.scrollBy(-slideValue, 0);
      }
    },
    scrollToEnd() {
      this.slideBox.scrollBy(this.slideWidth, 0);
    },
  },
};
</script>
