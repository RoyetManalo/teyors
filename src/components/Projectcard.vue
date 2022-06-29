<template>
  <div class="project-card">
    <h2>{{ text }}</h2>
    <div class="project-card-container">
      <img :src="src" alt="" />
      <div class="action">
        <a @click="openProject">View</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Projectcard",
  props: {
    text: String,
    src: String,
    paramname: String,
  },
  components: {},
  methods: {
    openProject() {
      this.$router.push(`/projects/${this.paramname}`);
    },
  },
};
</script>

<style scoped>
.project-card {
  background: #fff;
  padding: 1.5rem;
  cursor: pointer;
  color: #16484b;
}

.project-card-container {
  position: relative;
}

.action {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.8);
  display: flex;
  justify-content: center;
  align-items: center;
  opacity: 0;
  transition: 0.5s;
}

.project-card-container .action a {
  display: inline-block;
  color: #fff;
  border: #fff 2px solid;
  padding: 5px 15px;
  text-decoration: none;
}

.project-card-container:hover .action {
  opacity: 1;
}

img {
  max-width: 100%;
}

h2 {
  margin-bottom: 2rem;
}
</style>
