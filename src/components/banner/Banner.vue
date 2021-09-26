<template>
  <div class="banner">
    <Form />
  </div>
</template>

<script>
import "./Banner.css";
import QuotationForm from "../quotation/quotationForm/QuotationForm.vue";
export default {
  name: "Banner",
  components: {
    Form: QuotationForm,
  },
};
</script>
