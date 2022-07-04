<template>
  <Header />
  <div class="project-full">
    <div class="container">
      <h1>{{ getTitle }}</h1>
      <div class="description">
        <p class="left">{{ description }}</p>
      </div>
      <div class="stack-link flex m-2">
        <div class="stack">
          <h2 class="left">Tech Stack</h2>
          <div class="techStack flex">
            <div v-for="stack in stacks" class="stacks">
              {{ stack }}
            </div>
          </div>
        </div>
        <div class="link">
          <div class="flex m-1">
            <a :href="liveLink" target="_blank">
              <i class="fas fa-code"></i> Live Demo</a
            >
          </div>
          <div class="flex m-1">
            <a :href="githubLink" target="_blank"
              ><i class="fab fa-github"></i>Source Code</a
            >
          </div>
        </div>
      </div>
      <div class="image">
        <img :src="img" alt="" />
      </div>

      <div class="reason m-2">
        <h2 class="left">Why I Built This?</h2>
        <p class="left">{{ reason }}</p>
      </div>

      <!-- <div class="note">
        <h3 class="left m-1">Note:</h3>
        <p class="left">
          This is a personal project of mine to learn and improve my skills and
          knowledge in full stack development
        </p>
      </div> -->
    </div>
  </div>
</template>

<script>
import Header from "../components/Header.vue";
export default {
  name: "ProjectFull",
  data() {
    return {
      title: "",
      description: "",
      stacks: [],
      img: "",
      reason: "",
      liveLink: "",
      githubLink: "",
    };
  },
  props: {
    text: String,
    src: String,
    paramname: String,
  },
  components: {
    Header,
  },
  methods: {
    openProject() {
      this.$router.push(`/projects/${this.paramname}`);
    },
  },

  computed: {
    getTitle() {
      let params = this.$route.params.params;
      var newStr = params.replace(/-/g, " ");
      return newStr;
    },
  },

  created() {
    if (this.$route.params.params === "Student-Management-System") {
      this.title = "Student Management System";
      this.description =
        "A system that allows teacher to manage their student data, like recording the student attendance and grades and also the student personal information. The admin or the teacher has access in creating, editing, deleting and viewing the student's data";
      this.img = `${require("@/assets/projects/SMS.jpg")}`;
      this.reason =
        "As I go back into programming, this is my first full stack app, I built this to apply and test my skills in building full stack webapps using HTML, CSS, Javascript, PHP and MYSQL";
      this.stacks = ["Javascript", "PHP", "HTML", "CSS"];
      this.liveLink =
        "https://github.com/RoyetManalo/Student-Management-System-PHP";
      this.githubLink =
        "https://github.com/RoyetManalo/Student-Management-System-PHP";
    } else if (this.$route.params.params === "Alarmeme-Clock") {
      this.description =
        "A Web-based alarm clock that shows different dancing memes when alarms fires off";
      this.title = "Alarmeme Clock";
      this.stacks = ["Vue.js", "Netlify"];
      this.img = `${require("@/assets/projects/Alarms.jpg")}`;
      this.reason =
        "This is my first project in Vue.js, the main reason I built this is to explore and learn how to use a Javascript Frontend Framework";
      this.liveLink = "https://alarmeme-clock.netlify.app/";
      this.githubLink = "https://github.com/RoyetManalo/ALARMEME-CLOCK";
    } else if (this.$route.params.params === "Queueing-System") {
      this.title = "Queueing System";
      this.description =
        "A QR-Based Queueing System for getting COVID-19 vaccine in my hometown. This is a personal project of mine to enhance my Vue JS and Express.js skills and knowledge. This system have an admin and client endpoint, the admin has access to the creating, editing, deleting and viewing a person's data, it also has access to what brand of vaccine is available for a person to take. The client can fill up the information sheet for their pre-vaccine queue card, it includes firstname, lastname, age, vaccine brand and dose number. Then it was recorded in the admin database and the client will get a pdf file that has a QR Code and all of their info. The admin will scan the QR Code to verify that they are in the right queue number";
      this.stacks = ["Vue.js", "Express.js", "Mongodb", "Heroku"];
      this.img = `${require("@/assets/projects/QS.png")}`;
      this.reason =
        "The idea about building this software is because of my frustration on how my local health care center handle the queue of people that want to get the COVID-19 vaccine. They are just giving a piece of paper with number to determine whose in the current queue. In my mind what if there software that can solve this problem using QR Code, someone in the health care will only have to scan a QR Code and the system will verify it, and so the people in queue will spend less time standing and waiting for them to be called. So I decided to built this webapps that will solve this problem";
      this.liveLink = "https://sehcqs.herokuapp.com/";
      this.githubLink =
        "https://github.com/RoyetManalo/Vue-QR-Based-Queueing-System";
    } else if (this.$route.params.params === "Quick-Peek") {
      this.title = "Quick Peek";
      this.description =
        "A Website that developers can store all their code snippets and they can also view what snippets other developers have";
      this.stacks = ["React.js", "Express.js", "Mongodb", "Heroku"];
      this.img = `${require("@/assets/projects/QP.jpg")}`;
      this.reason =
        "As a developer myself. I sometimes forgot how to do certain this while developing a software, and I know I’m not the only one who encounter this kind of problem. A lot of you will say, “that’s why there’s a documentation,and stackoverflow for you to get the answer that you’re looking for in dealing with your development problems that you may encounter along the way. But what if there is a dedicated platform where us developers can store all our code snippets for future purposes and also see what others developers code snippets is.";
      this.liveLink = "https://quickpeek.herokuapp.com/";
      this.githubLink = "https://github.com/RoyetManalo/QuickPeek";
    }
  },
};
</script>

<style scoped>
.project-full {
  /* overflow: hidden; */
  padding: 3rem 6rem;
  cursor: pointer;
  color: #fff;
  box-sizing: border-box;
}

p {
  font-size: 1.2rem;
}
.container {
  max-width: 1000px;
  width: 100%;
  margin: 0 auto;
}
.flex {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.left {
  text-align: left;
}

.m-2 {
  margin: 2rem 0;
}
.m-1 {
  margin: 1rem 0;
}

.image {
  border: 1px solid #fff;
  border-radius: 20px;
  margin: auto;
  padding: 1rem;
}

.stacks {
  border: 1px solid #fff;
  border-radius: 10px;
  padding: 5px;
  margin-right: 5px;
}

.stack {
  justify-self: left;
}

.links div {
  margin-bottom: 1rem;
}
a {
  color: #fff;
  text-decoration: none;
  font-size: 1.2rem;
}

i {
  margin-right: 1rem;
}

img {
  width: 700px;
  max-width: 100%;
}
h1 {
  color: #fff;
  margin-bottom: 2rem;
  font-family: Chalk;
}

h2 {
  margin-bottom: 2rem;
}

/* Mobile */

@media (max-width: 480px) {
  .project-full {
    padding: 3rem;
  }

  .stack-link {
    display: block;
  }

  .stack h2 {
    text-align: center;
  }

  .link {
    display: flex;
    justify-content: space-between;
    margin-top: 1rem;
  }

  .techStack {
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
  }

  p {
    font-size: 1rem;
  }
}
</style>
