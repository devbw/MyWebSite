<template>
  <div class="background">
    <Menu />
    <div class="spinner">
      <span></span>
      <span></span>
      <span></span>
      <h1>Contact</h1>
    </div>
    <div class="container__form">
      <div class="links">
        <i class="fab fa-github" @click="openGit()"></i>
        <i class="fab fa-linkedin" @click="openLk()"></i>
        <a href="mailto:wullaertbrian@gmail.com"><i class="fas fa-paper-plane"></i></a>
      </div>
    </div>
  </div>
</template>

<script>
import Menu from "@/components/Menu.vue";
export default {
  name: "Contact",
  components: {
    Menu,
  },
  methods: {
    openGit(){
      window.open("https://github.com/devbw");
    },
    openLk(){
      window.open("https://www.linkedin.com/in/brianwullaertdev/");
    },
  }
};
</script>

<style scoped>
a{
  color: white;
}
.container__form {
  width: 100%;
  display: flex;
  justify-content: center;
  margin-top: 1rem;
}
.fab, .fas{
  font-size: 2rem;
  margin: 2rem 2.5rem;
  cursor: pointer;
  transition: .5s;
}
.fab:hover, .fas:hover{
  transform: rotate(360deg);
  color: #bd3bb6;
}
.links{
  margin-top: 1rem;
}
.spinner{
  margin: 10rem auto 0 auto;
}
</style>
