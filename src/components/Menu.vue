<template>
  <div>
    <nav>
      <router-link tag="div" class="link" to="/">DEVBW.</router-link>
      <div class="links">
        <router-link tag="p" class="link" to="/">About</router-link>
        <router-link tag="p" class="link" to="/skills">Skills</router-link>
        <router-link tag="p" class="link" to="/projects">Projects</router-link>
        <router-link tag="p" class="link" to="/contact">Contact</router-link>
      </div>
      <button class="site__btn">Click here</button>
    </nav>
    <modale :afficher="afficher" :toggleModale="toggleModale"></modale>
    <div class="menu">
      <router-link tag="div" class="link" to="/">DEVBW.</router-link>
      <i class="fas fa-bars" @click="toggleModale()"></i>
    </div>
  </div>
</template>

<script>
import Modale from '@/components/Modale.vue'

export default {
  name: 'Menu',
  components: {
    Modale,
  },
  data() {
    return {
      afficher: false,
    }
  },
  methods: {
    toggleModale() {
      this.afficher = !this.afficher;
    },
  }
}
</script>

<style>
nav{
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 90%;
  margin: auto;
  padding: 1rem 0;
  top: 0;
  left: 0;
  right: 0;
  position: fixed;
  background: #1d2026;
}
button{
  height: 30px;
  padding: 0 1rem;
  border: none;
  border-radius: 10px;
  cursor: pointer;
  background: #bd3bb6;
  color: #FFF;
  transition: 0.7s;
}
.links{
  display: flex;
}
.link{
  transition: all 0.7s;
  cursor: pointer;
}
.link:hover{
  transform: translateY(10px);
  color: #bd3bb6;
}
p{
  margin: 0 1rem;
}
.fas{
  font-size: 1.5rem;
}
.menu{
  display: none;
}
.modale{
  width: 100%;
  height: 100%;
}
.color__btn{
  background:#bd3bb6;
}
.site__btn{
  background:#bd3bb6;
  color: #FFF;
  transition: .5s;
}
.site__btn:hover{
  transform: translateY(10px)
}
@media (max-width: 600px) {
  nav{
    display: none;
  }
  .menu{
    display: flex;
    justify-content: space-between;
    position: fixed;
    top: 0;
    padding: 1rem 0;
    width: 90%;
    z-index: 10;
    background: #1d2026;
  }
}
</style>