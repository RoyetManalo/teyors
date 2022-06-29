<template>
  <div class="circles">
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>
  </div>
</template>

<script>
export default {
  name: "Braincells",
};
</script>

<style scoped>
.circles {
  position: absolute;
  top: 0;
  left: 0;
  width: 18%;
  height: 40%;
  overflow: hidden;
}

.circles div {
  position: absolute;
  display: block;
  width: 20px;
  height: 20px;
  background: #fff;
  bottom: -150px;
  animation: move 15s linear infinite;
}
.circles div:nth-child(1) {
  left: 20%;
  animation-delay: 0s;
}
.circles div:nth-child(2) {
  left: 35%;
  animation-delay: 3s;
}
.circles div:nth-child(3) {
  left: 45%;
  animation-delay: 2s;
}
.circles div:nth-child(4) {
  left: 55%;
  animation-delay: 4s;
}
.circles div:nth-child(5) {
  left: 65%;
  animation-delay: 2.5s;
}
.circles div:nth-child(6) {
  animation-delay: 5s;
  left: 75%;
}
.circles div:nth-child(7) {
  left: 85%;
  animation-delay: 3.5s;
}
.circles div:nth-child(8) {
  right: 10%;
  animation-delay: 1.5s;
}
.circles div:nth-child(9) {
  left: 50%;
  animation-delay: 5.5s;
}
.circles div:nth-child(10) {
  right: 25%;
  animation-delay: 3.3s;
}
.circles div:nth-child(11) {
  left: 15%;
  animation-delay: 3.8s;
}
.circles div:nth-child(12) {
  left: 35%;
  animation-delay: 6s;
}

@keyframes move {
  from {
    opacity: 1;
    border-radius: 0;
    transform: translateY(0) rotate(0deg);
  }
  to {
    opacity: 0;
    border-radius: 50%;
    transform: translateY(-800px) rotate(720deg);
  }
}

@media (max-width: 480px) {
  .circles {
    width: 50%;
  }
}
</style>
