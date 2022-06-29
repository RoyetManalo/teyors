<template>
  <div class="container">
    <div class="image">
      <img src="../assets/img/Laptopthin.png" alt="" />
      <div class="text active">
        <h2>Interest and hobbies</h2>
        <h3>When I’m not coding, here’s what I’m probably doing:</h3>
        <ul>
          <li>Playing Computer Games</li>
          <li>
            Watching TV Series, Animes, Documentaries, History content
            Educational content and some random sh*ts on the internet
          </li>
          <li>Doing physical sports (Basketball, table tennis, biking)</li>
        </ul>
      </div>
      <div class="text">
        <h2>Random Facts</h2>
        <ul>
          <li>Im a bit of a clown - i like making people laugh</li>
          <li>I’m a foodie - i like to cook but i like eating more</li>
          <li>Drawerist- i like to draw but im not good at it</li>
          <li>Metalhead - i found something calming in metal music</li>
        </ul>
      </div>
      <div class="buttons">
        <i class="fas fa-chevron-left" @click="prev"></i>
        <i class="fas fa-chevron-right" @click="next"></i>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Laptop",
  data() {
    return {
      isActive: false,
    };
  },
  methods: {
    scroll() {
      console.log("scroll");
    },
    prev() {},
  },
};
</script>

<style scoped>
.container {
  max-width: 1000px;
  margin: 0 auto;
  width: 100%;
}

ul {
  list-style: none;
}

li {
  text-align: left;
  margin-bottom: 1rem;
}

img {
  /* width: 10%; */
  /* animation: gobig 5s; */
  max-width: 100%;
}
.image {
  position: relative;
}

.text {
  display: none;
  position: absolute;
  top: 10%;
  left: 52%;
  transform: translateX(-50%);
  width: 60%;
  padding: 1rem;
}

.active {
  display: block;
}

h2,
h3 {
  text-align: left;
  margin-bottom: 1rem;
}

.buttons {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 50%;
  position: absolute;
  bottom: 22%;
  left: 52%;
  transform: translateX(-50%);
}

i {
  font-size: 8rem;
  color: #fff;
  cursor: pointer;
}

/* @keyframes gobig {
  from {
    width: 10%;
  }

  to {
    width: 100%;
  }
} */
</style>
