<template>
  <header class="header">
    <p class="header__phone">(21) 2042-4442</p>
    <div class="header__logo">Logo</div>
  </header>
  <Button @click="toggleQuotation" />
  <ContainerForm v-if="open" @toggleQuotation="toggleQuotation" />
</template>

<script>
import "./Header.css";
import QuotationSolicitationButton from "../quotation/quotationSolicitationButton/QuotationSolicitationButton.vue";
import QuotationWrapper from "../quotation/quotationWrapper/QuotationWrapper.vue";
export default {
  name: "Header",
  components: {
    Button: QuotationSolicitationButton,
    ContainerForm: QuotationWrapper,
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
