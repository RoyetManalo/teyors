<template>
  <section id="contacts">
    <div class="title">You can contact me through this:</div>
    <div class="content flex">
      <div class="email flex">
        <img src="../assets/img/email.png" alt="" /> contact@royetmanalo.com
      </div>
      <div class="cv">
        <router-link to="#" class="link flex"
          ><img src="../assets/img/dl.png" alt="" />Download my cv</router-link
        >
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Contacts",
};
</script>

<style scoped>
#contacts {
  padding: 2rem;
}
.title {
  font-size: 2rem;
  margin-bottom: 2rem;
}

.content {
  font-size: 2rem;
}

.flex {
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.link {
  color: #fff;
  text-decoration: none;
}

.cv:hover {
  transform: scale(1.2);
}

@media (max-width: 1024px) {
  #contacts .title {
    font-size: 1.8rem;
  }

  #contacts .email,
  #contacts .link {
    justify-content: flex-start;
    font-size: 1.5rem;
  }

  #contacts img {
    width: 60px;
  }
}

/* Tablet */
@media (max-width: 768px) {
  #contacts .title {
    font-size: 1.5rem;
  }
  #contacts .email,
  #contacts .link {
    justify-content: flex-start;
    font-size: 1.2rem;
  }

  #contacts .content {
    font-size: 1.5rem;
  }

  #contacts img {
    width: 50px;
  }
}

@media (max-width: 600px) {
  #contacts .content {
    display: block;
  }
  #contacts img {
    margin-right: 1rem;
  }
}

/* mobile */
@media (max-width: 480px) {
  #contacts .title {
    font-size: 1.2rem;
  }

  #contacts .content {
    display: block;
  }

  #contacts .email,
  #contacts .link {
    justify-content: flex-start;
    font-size: 1rem;
  }

  #contacts img {
    margin-right: 1rem;
  }
}
</style>
