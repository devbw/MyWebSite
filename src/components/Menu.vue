<template>
  <div>
    <nav>
      <div>DEVBW.</div>
      <div class="links">
        <p class="link">About</p>
        <p class="link">Skills</p>
        <p class="link">Projects</p>
        <p class="link">Contact</p>
      </div>
      <button class="link">Click here</button>
    </nav>
    <modale :afficher="afficher" :toggleModale="toggleModale"></modale>
    <div class="menu">
      <div>DEVBW.</div>
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
  margin-top: 1rem;
  top: 0;
  left: 0;
  right: 0;
  position: fixed;
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
@media (max-width: 600px) {
  nav{
    display: none;
  }
  .menu{
    display: flex;
    justify-content: space-between;
    position: fixed;
    padding: 1rem;
    top: 0;
    left: 0;
    right: 0;
    background: #1d2026;
    z-index: 1;
  }
}
</style>