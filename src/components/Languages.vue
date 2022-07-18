<template>
  <section class="languages">
    <div class="container flex">
      <div class="card">
        <h4>HTML5</h4>
        <!-- <img src="../assets/logos/html.png" alt="" /> -->
      </div>
      <div class="card">
        <h4>CSS3</h4>
        <!-- <img src="../assets/logos/css.png" alt="" /> -->
      </div>
      <div class="card">
        <h4>Javascript</h4>
        <!-- <img src="../assets/logos/js.png" alt="" /> -->
      </div>
      <div class="card">
        <h4>Typescript</h4>
        <!-- <img src="../assets/logos/js.png" alt="" /> -->
      </div>
      <div class="card">
        <h4>React.js</h4>
        <!-- <img src="../assets/logos/React.png" alt="" /> -->
      </div>
      <div class="card">
        <h4>Vue.js</h4>
        <!-- <img src="../assets/logos/Vue.png" alt="" /> -->
      </div>
      <div class="card">
        <h4>Node.js</h4>
        <!-- <img src="../assets/logos/node.png" alt="" /> -->
      </div>
      <div class="card">
        <h4>Express.js</h4>
        <!-- <img src="../assets/logos/express.png" alt="" /> -->
      </div>
      <div class="card">
        <h4>Mongodb</h4>
        <!-- <img src="../assets/logos/mongo.png" alt="" /> -->
      </div>
      <div class="card">
        <h4>Graphql</h4>
        <!-- <img src="../assets/logos/mongo.png" alt="" /> -->
      </div>
      <div class="card">
        <h4>PHP</h4>
        <!-- <img src="../assets/logos/php.png" alt="" /> -->
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
.container {
  max-width: 500px;
  margin: 0 auto;
  overflow: auto;
  padding: 20px 40px;
  /* width: 300px; */
}

.flex {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
}

.card {
  /* background: #fff; */
  border: 2px solid #fff;
  color: #fff;
  border-radius: 10px;
  box-shadow: 0 3px 10px rgba(0, 0, 0, 0.2); /* Horizontal offset, Vertical offset , Blur , color*/
  padding: 10px;
  cursor: pointer;
  /* margin: 10px; */
}

.languages .flex {
  flex-wrap: wrap;
  width: 380px;
}

.languages .card {
  text-align: center;
  /* margin: 18px 10px 40px; */
  margin: 6px 3px;
  transition: transform 0.2s ease-in;
}

.languages .card h4 {
  font-size: 20px;
  /* margin-bottom: 10px; */
}

.languages .card:hover {
  transform: translateY(-15px);
}

@media (max-width: 400px) {
  .languages .card h4 {
    font-size: 15px;
  }
}
</style>
