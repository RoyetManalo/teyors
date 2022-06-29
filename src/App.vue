<template>
  <div class="container">
    <router-view></router-view>
    <Footer />
  </div>
</template>

<script>
import Footer from "./components/Footer.vue";

export default {
  components: { Footer },
};
</script>

<style>
/* html {
  scroll-behavior: smooth;
} */
@font-face {
  font-family: Chalk;
  src: url("./assets/font/KGBrokenVesselsSketch.ttf");
}

@import url("https://fonts.googleapis.com/css2?family=Open+Sans&display=swap");
#app {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;
  background: #000;
  /* scroll-behavior: smooth; */
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.container {
  max-width: 1600px;
  width: 100%;
  margin: 0 auto;
}
</style>
