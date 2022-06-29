<template>
  <section id="landing">
    <Header />
    <Social class="social" />
    <div class="content flex">
      <div class="text">
        <h1>Hi, I’m Royet Manalo</h1>
        <h3>Software Engineer</h3>
        <p>I love coding and learning cool stuff 😎</p>
        <p>I build full stack webapps 👨‍💻</p>
        <p>I’m also a gamer 🎮</p>
      </div>
    </div>
    <div class="image" @click="change">
      <Stacks class="stacks" :draw="draw" />
      <img src="../assets/img/landing.png" alt="" v-if="draw" class="medraw" />
      <img src="../assets/img/rlanding.png" alt="" v-else />
    </div>
  </section>
</template>

<script>
import Header from "../components/Header.vue";
import Stacks from "../components/Stacks.vue";
import Social from "../components/Social.vue";
export default {
  name: "Landing",
  components: {
    Header,
    Stacks,
    Social,
  },
  data() {
    return {
      draw: true,
    };
  },

  methods: {
    change() {
      this.draw = !this.draw;
    },
  },
};
</script>

<style scoped>
/* Utility */

.flex {
  display: flex;
  justify-content: flex-start;
  align-items: center;
}

#landing {
  position: relative;
  color: #fff;
  height: 100vh;
  width: 100%;
  border-bottom: 1px solid #fff;
  /* overflow: hidden; */
}

#landing .image {
  position: absolute;
  bottom: -0.5rem;
  right: 1rem;
  display: flex;
  justify-content: flex-end;
  align-items: flex-end;
  height: 80%;
  cursor: pointer;
}

#landing .image img {
  max-width: 100%;
  width: 550px;
  animation: fadein 2s;
}

#landing .content {
  width: 60%;
  padding-left: 6rem;
}

#landing .text {
  padding-top: 7rem;
}

#landing .text h1 {
  font-size: 4.5rem;
  text-align: left;
  margin-bottom: 2rem;
}
#landing .text h3 {
  margin-bottom: 2rem;
  font-size: 2rem;
  text-align: left;
}

#landing h1,
#landing h3 {
  font-family: Chalk;
}
#landing .text p {
  font-size: 1.2rem;
  text-align: left;
}

#landing .stacks {
  position: absolute;
  bottom: 7rem;
  left: 1rem;
  /* transform: translateX(-50%); */
}
#landing .social {
  position: absolute;
  bottom: 5rem;
  left: 6rem;
}

@keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@media (max-height: 900px) {
  #landing .image img {
    width: 500px;
  }

  #landing .stacks {
    bottom: 6rem;
    left: 0rem;
  }
}

@media (max-width: 1400px) {
  #landing .image img {
    width: 500px;
  }

  #landing .stacks {
    bottom: 6rem;
    left: 2rem;
  }

  .content {
    padding: 0 5rem;
  }

  #landing .text h1 {
    font-size: 4rem;
  }
}
@media (max-width: 1200px) {
  #landing .text {
    /* padding-left: 2rem; */
  }
  #landing .text h1 {
    font-size: 3.5rem;
  }
}
/* Small Screen / Laptops */
@media (max-width: 1024px) {
  #landing .text h1 {
    font-size: 3rem;
  }
  #landing .text h3 {
    font-size: 2rem;
  }
  #landing .text h3 {
    font-size: 1.8rem;
  }
  #landing .text p {
    font-size: 1.1rem;
  }
}

/* tablet */
@media (max-width: 768px) {
  #landing .content {
    width: 100%;
  }
  #landing .image img {
    width: 400px;
    margin: 0 auto;
  }

  #landing .image {
    padding: 0;
    height: 60%;
  }

  #landing .stacks {
    bottom: 3rem;
    left: 0rem;
  }

  #landing .social {
    /* bottom: 1rem;
    left: 1rem;
    display: flex;
    flex-direction: column;
    gap: 1.2rem; */
    /* display: none; */
  }

  .content {
    display: block;
  }

  .content .text {
    padding: 2rem 0 !important;
  }

  .content .text h1 {
    text-align: left !important;
  }
  #landing .content .text h3 {
    font-size: 1.4rem;
    text-align: left;
  }
  #landing .content .text p {
    /* display: none; */
    text-align: left;
    font-size: 0.9rem;
  }
}

/* Mobile */
@media (max-width: 480px) {
  #landing .text h1 {
    font-size: 2rem;
    text-align: center !important;
  }
  #landing .text h3 {
    font-size: 1rem;
    text-align: center !important;
  }
  #landing .text p {
    text-align: center !important;
  }

  #landing .image {
    width: 90%;
    height: 50%;
  }
  #landing .image img {
    width: 300px;
  }

  #landing .content {
    display: block;
    padding: 0 2rem;
    margin-top: 2rem;
  }

  #landing .stacks {
    bottom: 2rem;
    left: 5.5rem;
  }

  #landing .social {
    display: none;
  }
}

@media (max-width: 440px) {
  #landing .stacks {
    left: 4rem;
  }
}
@media (max-width: 390px) {
  #landing .stacks {
    left: 3rem;
  }
}

@media (max-width: 480px) and (max-height: 700px) {
  .medraw {
    opacity: 0.5;
  }
}
</style>
