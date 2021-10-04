<template>
  <div class="bloc-modale" v-if="afficher">
    <div class="modale">
      <div class="quit">
        <i class="fas fa-times" @click="toggleModale"></i>
      </div>
      <div class="container__spinner">
        <div class="spinner">
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>
      <div class="links fade-in-bottom">
        <router-link tag="h2" to="/">About</router-link>
        <router-link tag="h2" to="/Skills">Skills</router-link>
        <router-link tag="h2" to="/Projects">Projects</router-link>
        <router-link tag="h2" to="/contact">Contact</router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Modale",
  props: {
    afficher: {
      type: Boolean,
      required: true,
    },
    toggleModale: {
      type: Function,
      required: true,
    },
  },
};
</script>

<style scoped>
.modale {
  box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.23);
  display: flex;
  flex-direction: column;
  width: 100%;
  min-height: 300px;
  position: fixed;
  background-color: #1d2026;
  justify-content: center;
}
.quit{
  position: fixed;
  top: 0;
  width: 100%;
}
.links {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  position: fixed;
}
.bloc-modale {
  position: fixed;
  z-index: 2;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  display: flex;
  justify-content: center;
  align-items: center;
}
h2 {
  color: #FFF;
  padding: 10px;
  cursor: pointer;
}
.overlay {
  background: rgba(0, 0, 0, 0.5);
  position: fixed;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
}
.fas {
  color: white;
}
.quit {
  display: flex;
  justify-content: right;
  padding: 1rem;
  z-index: 1;
  cursor: pointer;
}
.git{
  padding: 1rem 2rem;
  height: 50px;
}
.container__spinner{
  display: flex;
  flex-direction: column;
  align-items: center;
  opacity: .2;
}
.spinner{
  position: relative;
  width: 240px;
  height: 240px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.spinner span{
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: 2px solid white;
  pointer-events: none;
  animation: animate 15s linear infinite;
}
.spinner span:nth-child(1){
  border-radius: 30% 70% 70% 30% / 30% 30% 70% 70% ;
  border-color: #1fceed;
}
.spinner span:nth-child(2){
  animation-direction: reverse;
  border-radius: 74% 26% 42% 58% / 62% 65% 35% 38% ;
  border-color: #ed1fe3;
}
.spinner span:nth-child(3){
  animation-duration: 12s;
  border-radius: 49% 51% 26% 74% / 27% 29% 71% 73% ;
}
@keyframes animate
{
  0%
  {
    transform: rotate(0deg);
  }
  100%
  {
    transform: rotate(360deg);
  }
}
</style>
