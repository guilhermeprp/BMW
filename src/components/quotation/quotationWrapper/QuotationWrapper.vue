<template>
  <div class="quotation__wrapper">
    <button
      type="button"
      class="quotation__wrapper__close__button"
      @click="close"
    >
      Minimizar
    </button>
    <div class="quotation__form__container">
      <Form />
    </div>
  </div>
</template>

<script>
import "./QuotationWrapper.css";
import QuotationForm from "../quotationForm/QuotationForm.vue";
export default {
  name: "QuotationWrapper",
  components: { Form: QuotationForm },
  methods: {
    close() {
      this.$emit("toggleQuotation");
    },
  },
};
</script>
