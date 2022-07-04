<template>
  <div class="header">
    <div class="menu" @click="toggleMenu">
      <i class="fas fa-bars"></i>
    </div>
    <div class="logo">
      <router-link to="/">
        <img src="../assets/img/Teyorslogo.png" alt=""
      /></router-link>
    </div>
    <nav class="nav">
      <ul @mouseover="hover" :class="{ show: isActive }">
        <div class="div" @mouseleave="unhover">
          <li>
            <router-link to="/about" id="about">about</router-link>
          </li>
          <img
            src="../assets/img/slash.png"
            alt=""
            v-show="abouthover"
            class="slash"
          />
        </div>
        <div class="div" @mouseleave="unhover">
          <li>
            <router-link to="/#projects" id="project">projects</router-link>
          </li>
          <img
            src="../assets/img/slash.png"
            alt=""
            v-show="projecthover"
            class="slash"
          />
        </div>
        <div class="div" @mouseleave="unhover">
          <li>
            <router-link to="/#contacts" id="contact">contacts</router-link>
          </li>
          <img
            src="../assets/img/slash.png"
            alt=""
            v-show="contacthover"
            class="slash"
          />
        </div>
        <div class="div" @mouseleave="unhover">
          <li>
            <a
              href="https://www.dropbox.com/s/khim2nj8eiy5jw5/Royet_Manalo_Software_Engineer_CV.pdf?dl=0"
              id="cv"
              target="_blank"
              >cv</a
            >
          </li>
          <img
            src="../assets/img/slash.png"
            alt=""
            v-show="cvhover"
            class="slash"
          />
        </div>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      abouthover: false,
      projecthover: false,
      contacthover: false,
      cvhover: false,
      isActive: false,
    };
  },
  methods: {
    hover(e) {
      const id = e.target.id;

      switch (id) {
        case "about":
          this.abouthover = true;
          break;
        case "projects":
          this.projecthover = true;
          break;
        case "contacts":
          this.contacthover = true;
          break;
        case "cv":
          this.cvhover = true;
          break;
      }
    },
    unhover() {
      this.abouthover = false;
      this.projecthover = false;
      this.contacthover = false;
      this.cvhover = false;
    },

    toggleMenu() {
      this.isActive = !this.isActive;
    },
  },
};
</script>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.5rem 5rem;
  color: #fff;
  position: relative;
}

.menu {
  display: none;
}

.logo {
  font-size: 1.5rem;
  cursor: pointer;
}

.logo img {
  width: 50px;
}
ul {
  display: flex;
}

li {
  list-style: none;
}
a {
  font-family: Chalk;
  text-decoration: none;
  text-transform: uppercase;
  margin: 0 1rem;
  color: #fff;
  cursor: pointer;
  font-size: 1.2rem;
}
.nav {
  /* padding-right: 4rem; */
  padding: 0;
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
}

.div {
  position: relative;
}

.slash {
  position: absolute;
  /* bottom: 50%; */
  left: 50%;
  transform: translateX(-50%);
}

/* Mobile */
@media (max-width: 768px) {
  .header {
    display: block;
    padding: 1.5rem 5rem 0;
  }

  .menu {
    display: block;
    position: absolute;
    right: 2rem;
    font-size: 1.8rem;
  }

  ul {
    display: block;
    position: absolute;
    top: 4rem;
    left: 0;
    background: rgb(255, 255, 255);
    width: 100%;
    transform: translateY(-500px);
    padding: 30px;
    opacity: 0.9;
    transition: transform 0.5s ease-in-out;
  }

  ul.show {
    transform: translateX(0px);
  }
  ul li {
    margin: 1rem 0;
  }

  ul li a {
    color: #000;
  }
}
</style>
