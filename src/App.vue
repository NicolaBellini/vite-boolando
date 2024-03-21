<!-- APP -->
<script>
import Header from "./components/HeaderVue.vue";
// ???? mi dice che il file è gia stato incluso, ho dovuto mettere mainVue perchè il mip vs code me lo segnava sbagliato
import Main from "./components/MainVue.vue";
import Footer from "./components/FooterVue.vue";

export default {
  components: {
    Header,
    Main,
    Footer,
  },
};
</script>

<template>
  <Header />
  <Main />
  <Footer />
</template>

<style lang="scss">
@use "./assets/scss/main.scss";
</style>
