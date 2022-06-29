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
  border: #fff solid 1px;
}

.item {
  grid-area: 1/1;
  line-height: 30px;
  text-align: center;
  animation: spin 10s var(--d, 0s) linear infinite; /* duration = 12s, number of item = 6 so a delay of 12/6 = 2s */
  transform: rotate(0) translate(100px) rotate(0);
  width: 90px;
}
@keyframes spin {
  100% {
    transform: rotate(1turn) translate(100px) rotate(-1turn);
  }
}

img {
  width: 90px;
}

@media (max-width: 1400px) {
  img {
    width: 80px;
  }
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
@media (max-width: 480px) {
  img {
    width: 40px;
  }
  #container {
    grid-template-columns: 30px;
    grid-template-rows: 30px;
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
