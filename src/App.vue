<template>
  <div id="app">
    <Header />
    <!-- <div
      class="div"
      :onscroll="scroll()"
      :class="this.ticking ? 'scrollTrue' : ''"
    ></div> -->
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer,
  },
  data() {
    return {
      ticking: false,
    };
  },
  methods: {
    scroll() {
      if (window.scrollY == 0) {
        this.ticking = true;
      } else this.ticking = false;
    },
  },
};
</script>

<style lang="scss">
@import "./style/generals.scss";
#app {
  font-family: "Montserrat", Arial, Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: white;
  overflow: hidden;
}

.div {
  height: 100px;
  width: 100%;
}
.scrollTrue {
  background-color: yellow;
}
</style>
