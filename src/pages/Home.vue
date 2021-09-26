<template>
  <Header />
  <Banner />
  <Body />
</template>

<script>
import Header from "../components/header/Header.vue";
import Banner from "../components/banner/Banner.vue";
import Body from "../components/body/Body.vue";
export default {
  name: "Home",
  components: {
    Header,
    Banner,
    Body,
  },
  props: {
    msg: String,
  },
};
</script>
