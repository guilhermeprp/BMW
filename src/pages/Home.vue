<template>
  <Header v-if="headerShow" />
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
      headerShow: false,
    };
  },
  mounted() {
    window.addEventListener("scroll", this.headerHandler);
    window.addEventListener("resize", this.resizeHandler);
    this.$nextTick(this.mobileHandler);
  },
  methods: {
    headerHandler() {
      if (window.innerWidth > 768) {
        this.headerShow = window.pageYOffset > 550;
      }
    },
    resizeHandler() {
      this.headerShow = window.innerWidth < 768;
    },
    mobileHandler() {
      this.headerShow = window.innerWidth < 768;
    },
  },
  props: {
    msg: String,
  },
};
</script>
