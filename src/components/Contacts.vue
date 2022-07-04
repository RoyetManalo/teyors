<template>
  <section id="contacts">
    <div class="title">You can contact me through this:</div>
    <div class="content flex">
      <div class="email">
        <a href="mailto:contact@teyors.com" class="emailLink flex">
          <img src="../assets/img/email.png" alt="" />
          contact@teyors.com</a
        >
      </div>
      <div class="cv">
        <a
          href="https://www.dropbox.com/s/khim2nj8eiy5jw5/Royet_Manalo_Software_Engineer_CV.pdf?dl=0"
          class="cvLink flex"
          target="_blank"
          ><img src="../assets/img/dl.png" alt="" class="dlPic" />Download my
          cv</a
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
  font-family: Chalk;
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

.cvLink {
  color: #fff;
  text-decoration: none;
}

.emailLink,
.cvLink {
  gap: 1rem;
}
.emailLink {
  color: #fff;
  text-decoration: none;
}

.email:hover.email img {
  transform: scale(1.2);
}

.cv:hover.cv .dlPic {
  transform: scale(1.2);
}

@media (max-width: 1024px) {
  #contacts .title {
    font-size: 1.8rem;
  }

  #contacts .emailLink,
  #contacts .cvLink {
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
  #contacts .emailLink,
  #contacts .cvLink {
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

  #contacts .emailLink,
  #contacts .cvLink {
    justify-content: flex-start;
    font-size: 1rem;
  }

  #contacts img {
    margin-right: 1rem;
  }
}
</style>
