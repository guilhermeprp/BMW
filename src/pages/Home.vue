<template>
  <Navbar />
  <Header v-if="show" />
  <Banner />
  <Body />
  <Footer />
  <Whatsapp v-if="show" />
  <Baseboard v-if="show" />
</template>

<script>
import {
  Navbar,
  Header,
  Banner,
  Body,
  Footer,
  FloatingActionButton,
  Baseboard,
} from "../components/index";

export default {
  name: "Home",
  components: {
    Navbar,
    Header,
    Banner,
    Body,
    Footer,
    Whatsapp: FloatingActionButton,
    Baseboard,
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
