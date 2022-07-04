<template>
  <footer class="footer flex">
    <div class="text">Design and built by: Royet Manalo</div>
    <div class="text">Copyright &copy; 2022</div>
  </footer>
</template>

<script>
export default {};
</script>

<style scoped>
.footer {
  padding: 1rem;
}
.flex {
  display: flex;
  justify-content: space-around;
  align-items: center;
}

@media (max-width: 480px) {
  .footer {
    display: block;
    font-size: 0.9rem;
  }
}
</style>
