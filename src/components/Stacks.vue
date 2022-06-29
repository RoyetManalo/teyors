<template>
  <div class="stacks">
    <div id="container" v-if="draw">
      <img
        src="../assets/whitestacks/white-mongo.png"
        alt=""
        class="item"
        style="--d: 0s"
      />
      <img
        src="../assets/whitestacks/white-express.png"
        alt=""
        class="item"
        style="--d: -2s"
      />
      <img
        src="../assets/whitestacks/white-node.png"
        alt=""
        class="item"
        style="--d: -4s"
      />
      <img
        src="../assets/whitestacks/white-vue.png"
        alt=""
        class="item"
        style="--d: -6s"
      />
      <img
        src="../assets/whitestacks/white-react.png"
        alt=""
        class="item"
        style="--d: -8s"
      />
    </div>
    <div id="container" v-else>
      <img
        src="../assets/stacks/mongo.png"
        alt=""
        class="item"
        style="--d: 0s"
      />
      <img
        src="../assets/stacks/express.png"
        alt=""
        class="item"
        style="--d: -2s"
      />
      <img
        src="../assets/stacks/node.png"
        alt=""
        class="item"
        style="--d: -4s"
      />
      <img
        src="../assets/stacks/vue.png"
        alt=""
        class="item"
        style="--d: -6s"
      />
      <img
        src="../assets/stacks/react.png"
        alt=""
        class="item"
        style="--d: -8s"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "Stack",
  components: {},
  props: {
    draw: Boolean,
  },
};
</script>

<style scoped>
/* make the revolving animation smooth */

#container {
  width: 300px;
  height: 300px;
  margin: 40px auto;
  display: grid;
  grid-template-columns: 30px;
  grid-template-rows: 30px;
  place-content: center;
  border-radius: 50%;
}

.item {
  grid-area: 1/1;
  line-height: 30px;
  text-align: center;
  animation: spin 10s var(--d, 0s) linear infinite; /* duration = 12s, number of item = 6 so a delay of 12/6 = 2s */
  transform: rotate(0) translate(100px) rotate(0);
}
@keyframes spin {
  100% {
    transform: rotate(1turn) translate(100px) rotate(-1turn);
  }
}

@keyframes tabletspin {
  100% {
    transform: rotate(1turn) translate(70px) rotate(-1turn);
  }
}

@keyframes mobilespin {
  100% {
    transform: rotate(1turn) translate(50px) rotate(-1turn);
  }
}

img {
  width: 80px;
}

@media (max-height: 900px) {
  img {
    width: 70px;
  }
}

@media (max-width: 1400px) {
  #container {
    grid-template-columns: 100px;
    grid-template-rows: 30px;
  }
}

@media (max-width: 1050px) {
  img {
    width: 70px;
  }
  #container {
    grid-template-columns: 100px;
    grid-template-rows: 10px;
  }
}

/* Tablet */

@media (max-width: 768px) {
  img {
    width: 60px;
  }
  .item {
    transform: rotate(0) translate(70px) rotate(0);
    animation: tabletspin 10s var(--d, 0s) linear infinite;
  }
}

/* Mobile */
@media (max-width: 480px) {
  .item {
    transform: rotate(0) translate(50px) rotate(0);
    animation: mobilespin 10s var(--d, 0s) linear infinite;
  }

  img {
    width: 40px;
  }
  #container {
    width: 200px;
    height: 200px;
  }
}

/* Tablet */

/* @media (max-width: 1200px) {
  img {
    width: 80px;
  }
  #container {
    grid-template-columns: 100px;
    grid-template-rows: 30px;
  }
} */
</style>
