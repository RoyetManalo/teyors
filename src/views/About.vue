<template>
  <Header />
  <div class="about">
    <div class="container">
      <h1 class="title">About me</h1>
      <section class="who mb-1">
        <h2 class="left mb-1">"Who are you? by the way” I’m glad you ask"</h2>
        <p class="left">
          Well, as you already saw when this site first load, my name is Royet
          Manalo, I’m from the province of Camarines Norte “the gateway to
          Bicolandia” in the beautiful country called Philippines. I have
          bachelors degree on Information Technology Major in Digital Arts from
          STI College Lucena. Currently, I do build webapps and websites
        </p>
      </section>
      <section class="how">
        <h2 class="left mb-1">
          My journey into the computer and technology world
        </h2>
        <div class="mb-1">
          <div class="text">
            <p class="left">
              I got exposed into computer games at an early age, if I remember
              it correctly I was 5 or 6 years old when I got my hands on an
              arcade game. I was so happy and excited at the same time when I’m
              playing on it, Im so good on it and I can beat a lot of kids twice
              my age in the arcade game. I inveted a lot of moves and combos
              from scratch, I can finish the stages, in a short period of time
              compared to other kids in my area.
            </p>
          </div>
          <img src="../assets/img/arcademe.png" alt="" />
        </div>
        <div class="mb-1">
          <div class="text">
            <p class="left">
              I realized that at an earlyage, I’m already solving problems and
              creating solution while playing games. I thinks that’s why when I
              got into software engineering, I really love solving problems and
              providing solutions, I love challenges and problems that make my
              me scratch my head, it only shows that I accept this challenges
              and I’m ready to find solutions to it.
            </p>
          </div>
        </div>
        <div class="mb-1">
          <h2 class="mb-1">First encounter in software development</h2>
          <p class="left mb-1">
            I was 15 when I first learn what HTML and CSS is, but during that
            time, I was just an observer who listen to the teacher and sometimes
            wrote HTML on a paper, because I dont have any access to any kind of
            computer at that time.
          </p>

          <p class="left mb-1">
            And when I got into college, thats when I learn Java as my first
            programming language, i dont fully understand the whole language of
            Java but the concept of programming is what I really understand.
          </p>
          <p class="left mb-1">
            After that I learned and I built a lot of things, first with
            Microsoft Visual Basic for Applications and Database Management
            System using Microsoft SQL Server, I built a Student Managemet
            System. Then I digitalized the Snake and Ladder Game using Visual
            Basic in Microsoft Excel. And then an android app that allows user
            to store all of their customers debt called “Debt Note” using
            Android Studio and SQLite.
          </p>
          <div class="image">
            <img src="../assets/img/College.png" alt="" class="college" />
            <p class="small">
              The only remants of the things that I built during college
            </p>
          </div>

          <p>
            I dont that have any copy of source code of all of the softwares
            that I built during college, cause my only laptop gave up on me, and
            I dont have any backup, back then I dont even know what Github is
            😅.
          </p>
        </div>
        <div>
          <h2>Hardest time of my life as an aspiring developer</h2>
          <p>
            2018 was time that I temporarily part ways with programming due to
            lack of access to a computer. I dont even know what I wanna do at
            that time, I was an intern at a Post Production Studio for Weddings
            as a Video Editor. Then I graduated in 2019, took a couple months of
            vacation then the pandemic hits, it sucks, I dont know what to do, I
            dont have any access to a computer, a lot is going through my mind
            at that time and I started to give up on my dreams and become very
            confused if I should pursue my passion or try another thing.
          </p>
          <img src="../assets/img/Bondok.png" alt="" class="rise" />
        </div>

        <div>
          <h2>A Glimpse of hope</h2>
          <p class="left">
            In 2021, my parents decided to buy a computer for my little brother,
            I was so happy at that time because I will be able to do software
            development again. I started searching and deciding what path should
            I take, then decided to go with web development, I started from zero
            and learning gets hard at first, but the knowledge that I got from
            college is still there so its not that hard for me to get back in
            software development. I learned HTML and CSS first, then Javascript
            and PHP. I recreated the Student Management System. After that I
            started to learn a framework, Vue.js then I build the Alarmeme and
            the QR-Based Queueing System, then React.js where I build Quick
            Peek. And here I am continuing the passion that I love and the
            career that I wanna have, learning more cool stuff from this world
            and see where it takes me.
          </p>
        </div>
      </section>
      <div class="line"></div>

      <section class="randomfacts">
        <div class="text">
          <div class="texts">
            <h2>Interest and hobbies</h2>
            <h3>When I’m not coding, here’s what I’m probably doing:</h3>
            <ul>
              <li>Playing Computer Games 🎮</li>
              <li>
                Watching TV Series, Animes, Documentaries, History content
                Educational content and some random sh*ts on the internet 📺
              </li>
              <li>
                Doing physical sports (Basketball 🏀, table tennis 🏓, biking
                🚴‍♂️)
              </li>
            </ul>
          </div>
          <div class="texts">
            <h2>Random Facts</h2>
            <ul>
              <li>Im a bit of a clown 🤡 - I like making other people laugh</li>
              <li>I’m a foodie 🍖 - I like to cook but i like eating more</li>
              <li>Drawerist ✏ - I like to draw but im not good at it</li>
              <li>Metalhead 🤘 - I found something calming in metal music</li>
            </ul>
          </div>
        </div>
      </section>
      <!-- <Laptop /> -->
    </div>
  </div>
</template>

<script>
import Header from "../components/Header.vue";
import Laptop from "../components/Laptop.vue";
export default {
  name: "About",
  components: {
    Header,
    Laptop,
  },
};
</script>

<style scoped>
.container {
  max-width: 1000px;
  margin: 0 auto;
  width: 100%;
}

.how {
  border-bottom: 2px solid #fff;
}

section {
  padding: 2rem 0;
}

p,
h2 {
  text-align: left;
  margin-bottom: 2rem;
}

p {
  font-size: 1.3rem;
  line-height: 1.6;
}

ul {
  list-style: none;
}

li {
  text-align: left;
  margin-bottom: 1rem;
}

h3 {
  text-align: left;
  margin-bottom: 1rem;
}

.small {
  font-size: 0.8rem;
  text-align: center;
  margin-top: 1rem;
  margin-bottom: 0;
}

h2 {
  font-size: 1.8rem;
  font-weight: bolder;
}

img {
  width: 300px;
}
.image {
  border: 1px solid #fff;
  border-radius: 20px;
  padding: 2rem;
  width: 90%;
  margin: 0 auto;
  margin-bottom: 2rem;
}

.image img {
  max-width: 100%;
}
.college {
  width: 800px;
}

.left {
  text-align: left;
}

.flex {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.texts {
  border: 1px solid #fff;
  padding: 1rem;
  margin: 0 auto;
  border-radius: 20px;
  margin-bottom: 1rem;
}

.rise {
  width: 100%;
  margin-bottom: 1.5rem;
}

.mb-1 {
  margin-bottom: 2rem;
}

.title {
  font-size: 3rem;
  text-align: left;
  margin-bottom: 2rem;
}

.randomfacts img {
  width: 500px;
}

@media (max-width: 1100px) {
  .about {
    padding: 3rem;
  }
}

@media (max-width: 900px) {
  .randomfacts img {
    width: 350px;
  }
}
/* Tablets */
@media (max-width: 768px) {
  .randomfacts img {
    display: none;
  }
}

/* Mobile */
@media (max-width: 480px) {
  .title {
    font-size: 2rem;
  }

  .about {
    padding: 2rem;
  }

  p {
    font-size: 1rem;
  }
  .randomfacts img {
    display: none;
  }
}
</style>
