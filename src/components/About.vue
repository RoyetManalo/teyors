<template>
  <section id="about">
    <div class="content">
      <div class="image" @click="change">
        <img src="../assets/img/me-smile.png" alt="" v-if="draw" />
        <img src="../assets/img/rme-smile.png" alt="" v-else />
      </div>

      <div class="text">
        <h1>Hey! That's me</h1>
        <p>
          I’m a graduate of Information Technology who really enjoy coding and
          love learning new things. I build websites and webapps. My love and
          passion about programming started during my freshman year in college,
          the feelings that I get when my program runs is unexplainable. And
          that is why here I am, continuing my passion because it makes me
          happy.
        </p>
        <router-link to="/about" class="readmore">Wanna know more?</router-link>
      </div>
    </div>

    <div class="skills">
      <h2 class="title">Things that is currently in my knowledge box</h2>
      <div class="skills-content">
        <Languages class="lang" />
        <Braincells class="cells" />
        <div class="skills-image" @click="schange">
          <img src="../assets/img/knowhead.png" alt="" v-if="sdraw" />
          <img src="../assets/img/rknowhead.png" alt="" v-else />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Languages from "../components/Languages.vue";
import Braincells from "../components/Braincells.vue";
export default {
  name: "About",
  components: {
    Languages,
    Braincells,
  },
  data() {
    return {
      draw: true,
      sdraw: true,
    };
  },

  methods: {
    change() {
      this.draw = !this.draw;
    },
    schange() {
      this.sdraw = !this.sdraw;
    },
  },
};
</script>

<style scoped>
#about {
  /* background: #16484b; */
  padding: 2rem 0;
  position: relative;
  color: #fff;
  border-bottom: 1px solid #fff;
}

#about .content {
  display: flex;
  justify-content: space-evenly;
  /* align-items: center; */
}

#about img {
  justify-self: flex-end;
  width: 550px;
  animation: fadein 2s;
}

#about .content .text {
  width: 40%;
  font-size: 1.3rem;
  text-align: left;
  padding-top: 8rem;
}

h1 {
  margin-bottom: 2rem;
  font-family: Chalk;
}

.readmore {
  display: inline-block;
  color: #fff;
  text-decoration: none;
  margin-top: 2rem;
}

.flex {
  display: flex;
  justify-content: space-around;
}
.title {
  margin: 1.5rem 0;
  font-family: Chalk;
}
.skills-content {
  position: relative;
}
.skills-content img {
  margin-top: 12rem;
  animation: fadein 2s;
}

.skills-image,
.image {
  cursor: pointer;
}
.lang {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  z-index: 2;
}

.cells {
  position: absolute;
  left: 48%;
  bottom: 0%;
  transform: translateX(-50%);
  z-index: 1;
}

@keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

/* Small Screenms */
@media (max-width: 1024px) {
  #about img {
    width: 450px;
  }

  #about .content .text {
    padding-top: 5rem;
  }

  #about .skills-image img {
    padding-top: 3rem;
  }
}

/* Tablet */
@media (max-width: 768px) {
  #about img {
    width: 350px;
  }

  #about .skills-image img {
    padding-top: 5rem;
  }
  #about .content {
    display: block;
  }

  #about .content .text {
    width: 100%;
    padding: 1rem 3rem;
  }
}

/* Mobile */
@media (max-width: 480px) {
  #about .skills .title {
    font-size: 1.3rem;
    padding: 0 1.2rem;
  }

  p {
    font-size: 1rem;
  }
}
</style>
