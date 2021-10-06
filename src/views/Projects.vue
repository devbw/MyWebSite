<template>
  <div class="background">
    <Menu />
    <div class="container">
      <h1>Projects</h1>
      <p>Retrouvez ici, l'ensemble des projets sur lesquels j'ai travaillé !</p>
    </div>
    <div class="container__projets">
      <div class="projets" v-for="projet in projets" :key="projet.id">
        <div class="container__card">
          <div class="box">
            <div class="box__content">
              <h2>{{ projet.projet }}</h2>
              <h3>{{ projet.entreprise }}</h3>
              <p> {{ projet.descript }} </p>
              <div class="group__skills">
                <span v-for="skill in projet.techno" :key="skill.index"> {{ skill }} </span>
              </div>
              <a :href="projet.link" target="_blank" class="box__button">Site</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Menu from "@/components/Menu.vue";
import Projets from "@/assets/projects.json";

export default {
  name: "Projects",
  data() {
    return {
      projets: Projets,
      show: false,
    };
  },
  components: {
    Menu,
  },
  created() {
    this.getProjet();
  },
  methods: {
    getProjet() {
      console.log(this.projets);
    },
    getImgUrl(pic) {
      return require("../assets/pictures/" + pic);
    },
  },
};
</script>

<style scoped>
h1 {
  margin: 1rem;
}
h3 {
  color: #bd3bb6;
  margin: .2rem 0 .5rem 0;
}
a{
  text-decoration: none;
  color: #FFF;
}
p {
  margin: 0;
  text-align: center;
}
span{
  color:#66d3fa;
}
.container {
  width: 90%;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 10rem auto 1rem auto;
}
.container__card{
  margin: 0 1rem;
}
.container__projets {
  margin-top: 3rem;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}
.projets {
  margin: 1rem;
  transition: 0.5s;
}
.tech{
  color:#bd3bb6;
}
.box{
  position: relative;
  width: 250px;
  height: 400px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: auto;
  background: #1d2026;
  overflow: hidden;
  border-radius: .5rem;
}
.box::before{
  content: '';
  position: absolute;
  width: 200px;
  height: 120%;
  background: linear-gradient(#bd3bb6, #66d3fa);
  animation: animate 10s linear infinite;
}
.box::after:hover ~ .box::before{
  animation: animate 10s reverse infinite;
}
.box::after{
  content: '';
  position: absolute;
  inset: 4px;
  background: #1d2026;
  border-radius: .5rem;
}
.box__content{
  position: relative;
  color: #FFF;
  z-index: 1;
  display: flex;
  flex-direction: column;
  align-items: left;
  width: 80%;
}
.box__content p{
  text-align: left;
  font-size: 0.9rem;
}
.group__skills{
  display: flex;
  flex-wrap: wrap;
}
.group__skills span{
  margin: 0.3rem .5rem 0 0;
}
.box__button{
  margin: 1rem 0;
  background:#bd3bb6;
  text-align: center;
  border-radius: .5rem;
  transition: .3s;
}
.box__button:hover{
  transform: translateY(10px);
}
@keyframes animate {
  0%{
    transform: rotate(0deg);
  }
  100%{
    transform: rotate(360deg);
  }
}
</style>
