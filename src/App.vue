<script>
import Header from "./components/Header.vue";
// ???? mi dice che il file è gia stato incluso
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";

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

<style lang="scss"></style>
