<template>
  <div>
    <h1 class="body__title">ESCOLHA SEU BMW</h1>
    <CarsList />
  </div>
</template>

<script>
import "./Body.css";
import CarsList from "./subcomponents/carsList/CarsList.vue";
export default {
  name: "Body",
  components: {
    CarsList,
  },
};
</script>
