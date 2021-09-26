<template>
  <Header v-if="show" />
  <Banner />
  <Body />
  <Footer />
</template>

<script>
import Header from "../components/header/Header.vue";
import Banner from "../components/banner/Banner.vue";
import Body from "../components/body/Body.vue";
import Footer from "../components/footer/Footer.vue";
export default {
  name: "Home",
  components: {
    Header,
    Banner,
    Body,
    Footer,
  },
  data() {
    return {
      show: false,
    };
  },
  mounted() {
    window.addEventListener("scroll", this.scrollHandler);
    window.addEventListener("resize", this.resizeHandler);
    this.$nextTick(this.mobileHandler);
  },
  methods: {
    scrollHandler() {
      if (window.innerWidth > 768) {
        this.show = window.pageYOffset > 550;
      }
    },
    resizeHandler() {
      this.show = window.innerWidth < 768;
    },
    mobileHandler() {
      this.show = window.innerWidth < 768;
    },
  },
};
</script>
