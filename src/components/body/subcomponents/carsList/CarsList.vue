<template>
  <div class="choose__car__list">
    <div v-for="index in 8" :key="index" class="choose__car__wrapper">
      <div class="choose__car__img"></div>
      <h2 class="choose__car__name">BMW Série 1</h2>
      <div class="choose__car__row__button">
        <button class="choose__car__button__quotation" @click="toggleQuotation">
          Cotação
        </button>
        <button class="choose__car__button__call">Ligar</button>
      </div>
      <div class="choose__car__share">
        <p>Compartilhe:</p>
        <div>F</div>
        <div>W</div>
      </div>
    </div>
  </div>
  <QuotationWrapper v-if="open" @toggleQuotation="toggleQuotation" />
</template>

<script>
import QuotationWrapper from "../../../quotation/quotationWrapper/QuotationWrapper.vue";
import "./CarsList.css";
export default {
  name: "CarsList",
  components: {
    QuotationWrapper,
  },
  data() {
    return {
      open: false,
    };
  },
  methods: {
    toggleQuotation() {
      this.open = !this.open;
    },
  },
};
</script>
