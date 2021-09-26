<template>
  <div class="choose__car__wrapper">
    <div class="choose__car__img"></div>
    <h2 class="choose__car__name">BMW Série 1</h2>
    <slot></slot>
    <div class="choose__car__share">
      <p>Compartilhe:</p>
      <div>F</div>
      <div>W</div>
    </div>
  </div>
</template>

<script>
import "./CarCard.css";
export default {
  name: "CarCard",
};
</script>
