<template>
  <div class="choose__car__list">
    <CarCard v-for="index in 8" :key="index">
      <div class="choose__car__row__button">
        <button class="choose__car__button__quotation" @click="toggleQuotation">
          Cotação
        </button>
        <button class="choose__car__button__call">Ligar</button>
      </div>
    </CarCard>
  </div>
  <QuotationWrapper v-if="open" @toggleQuotation="toggleQuotation" />
</template>

<script>
import CarCard from "../carCard/CarCard.vue";
import QuotationWrapper from "../../../quotation/quotationWrapper/QuotationWrapper.vue";
import "./CarsList.css";
export default {
  name: "CarsList",
  components: {
    CarCard,
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
