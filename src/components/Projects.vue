<template>
  <section id="projects">
    <h2 class="title">Projects</h2>

    <div class="project-content">
      <div class="left">
        <h2 class="project-title">Student Management System</h2>
        <div class="text">
          A system that allows teacher to manage their student data.
        </div>
        <router-link to="/projects/Student-Management-System" class="view"
          >View Project</router-link
        >
      </div>
      <div class="right">
        <img src="../assets/projects/SMS.jpg" alt="" />
      </div>
    </div>

    <div class="project-content">
      <div class="left">
        <h2 class="project-title">Queueing System</h2>
        <div class="text">
          A QR-Based Queueing System for getting COVID-19 vaccine in my
          hometown.
        </div>
        <router-link to="/projects/Queueing-System" class="view"
          >View Project</router-link
        >
      </div>
      <div class="right">
        <img src="../assets/projects/QRSEHC.jpg" alt="" />
      </div>
    </div>
    <div class="project-content">
      <div class="left">
        <h2 class="project-title">Quick Peek</h2>
        <div class="text">
          A Website that developers can store all their code snippets and they
          can also view what snippets other developers have
        </div>
        <router-link to="/projects/Quick-Peek" class="view"
          >View Project</router-link
        >
      </div>
      <div class="right">
        <img src="../assets/projects/QP.jpg" alt="" />
      </div>
    </div>
    <div class="project-content">
      <div class="left">
        <h2 class="project-title">Alarmeme Clock</h2>
        <div class="text">
          An alarm clock that shows dancing memes when alarms fires off
        </div>
        <router-link to="/projects/Alarmeme-Clock" class="view"
          >View Project</router-link
        >
      </div>
      <div class="right">
        <img src="../assets/projects/Alarms.jpg" alt="" />
      </div>
    </div>
  </section>
</template>

<script>
import Projectcard from "../components/Projectcard.vue";
export default {
  name: "Projects",
  components: {
    Projectcard,
  },
  data() {
    return {
      sms: `${require("@/assets/projects/SMS.jpg")}`,
      alarm: `${require("@/assets/projects/Alarms.jpg")}`,
      qr: `${require("@/assets/projects/QRSEHC.jpg")}`,
      qp: `${require("@/assets/projects/QP.jpg")}`,
    };
  },
};
</script>

<style scoped>
#projects {
  color: #fff;
  padding: 2rem;
  position: relative;
  border-bottom: 1px solid #fff;
}

#projects .title {
  font-size: 1.7rem;
  margin: 1.5rem 0;
  font-family: Chalk;
}

.project-content {
  max-width: 1000px;
  margin: 0 auto;
  overflow: auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  text-align: left;
  margin-top: 1.5rem;
  margin-bottom: 1.5rem;
  border: 1px solid #fff;
  border-radius: 20px;
  padding: 30px;
  position: relative;
}

.project-content .left {
  width: 50%;
}

.project-content .left h2 {
  margin-bottom: 1.5rem;
  font-size: 1.5rem;
}

.project-content .left .text {
  margin-bottom: 1.5rem;
  font-size: 1.2rem;
}

.project-content img {
  width: 400px;
}

.view {
  display: inline-block;
  color: #fff;
  text-decoration: none;
  margin-top: 1rem;
  border: 1px solid #fff;
  border-radius: 20px;
  padding: 10px;
  /* position: absolute;
  bottom: 1.5rem; */
}
.view:hover {
  background: #fff;
  color: #000;
}

@media (max-width: 845px) {
  .project-content {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 768px) {
  #projects .project-content img {
    width: 400px;
    max-width: 100%;
    margin-top: 1rem;
  }
  #projects .project-content .left {
    width: 100%;
    padding: 1rem;
    padding-left: 0;
  }
}

@media (max-width: 480px) {
  .project-content {
    display: block;
  }

  img {
    margin-bottom: 3rem;
  }

  .project-content .left .text {
    margin-bottom: 0;
    font-size: 1rem;
  }
  #projects .project-content .view {
    text-align: center;
    position: absolute;
    width: 80%;
    bottom: 1rem;
    left: 2.5rem;
  }
}

@media (max-width: 400px) {
  #projects .project-content .view {
    width: 75%;
  }
}
@media (max-width: 360px) {
  #projects .project-content .view {
    width: 70%;
  }
}
</style>
