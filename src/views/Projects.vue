<template>
  <div class="background">
    <Menu />
    <div class="container">
      <h1>Projects</h1>
      <p>Retrouvez ici, l'ensemble des projets sur lesquels j'ai travaillé !</p>
    </div>
    <div class="container__projets">
      <div class="projets" v-for="projet in projets" :key="projet.id">
        <v-card class="mx-auto" max-width="270">
          <v-img :src="getImgUrl(projet.image)" height="200px" style="background: #000;"></v-img>

          <v-card-title>
            {{ projet.projet }}
          </v-card-title>

          <v-card-subtitle>
            {{ projet.entreprise }}
          </v-card-subtitle>

          <v-card-actions>
            <v-btn @click="show = !show" color="orange lighten-2" text>
              Voir +
            </v-btn>

            <v-spacer></v-spacer>

            <v-btn icon @click="show = !show">
              <i class="fas fa-mouse"></i>
            </v-btn>
          </v-card-actions>

          <v-expand-transition>
            <div v-show="show">
              <v-divider></v-divider>
              <v-card-subtitle>
                Description :
              </v-card-subtitle>
              <v-card-text>
                {{ projet.descript }}
              </v-card-text>
              <v-divider></v-divider>
              <v-card-subtitle>
                Technos :
              </v-card-subtitle>
              <div v-for="tech in projet.techno" :key="tech.index">
                <p class="tech">{{ tech }}</p>
              </div>
              <v-divider class="technos"></v-divider>
              <button class="site__btn"><a :href="projet.link" target="_blank">Site</a></button>
            </div>
          </v-expand-transition>
        </v-card>
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
h2 {
  color: #000;
}
h3 {
  color: #000;
}
a{
  text-decoration: none;
  color: #FFF;
}
p {
  margin: 0;
  text-align: center;
}
.container {
  width: 90%;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 10rem auto 1rem auto;
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
.sub__container {
  height: 100%;
  width: 100%;
}
.pic__projet {
  height: 100%;
}
.swiper {
  width: 600px;
  height: 300px;
}
.fas {
  color: #bd3bb6;
  transition: 0.8s;
}
.fas:hover {
  transform: rotate(360deg);
}
.site__btn{
  background:#bd3bb6;
  margin: 1rem;
  color: #FFF;
  transition: .5s;
}
.site__btn:hover{
  transform: translateY(10px)
}
.technos{
  margin-top: 1rem;
}
.tech{
  color:#bd3bb6;
}
</style>
