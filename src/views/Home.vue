<template>
  <div class="home">
    <Landing />
    <About />
    <Projects />
    <Contacts />
  </div>
</template>

<script>
// @ is an alias to /src
import Stacks from "../components/Stacks.vue";
import Header from "../components/Header.vue";
import Landing from "../components/Landing.vue";
import About from "../components/About.vue";
import Projects from "../components/Projects.vue";
import Languages from "../components/Languages.vue";
import Contacts from "../components/Contacts.vue";
import Footer from "../components/Footer.vue";

export default {
  name: "Home",
  components: {
    Stacks,
    Header,
    Languages,
    Landing,
    About,
    Projects,
    Contacts,
    Footer,
  },
};
</script>

<style scoped>
.home {
  /* background: #16484b; */
  /* background-image: url("../assets/img/building.png"); */
}

.building {
  width: 100%;
  /* overflow: hidden; */
}

.building .img {
  width: 10px;
}
</style>
