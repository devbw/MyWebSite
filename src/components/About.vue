<template>
  <div class="sontainer">
    <div class="spinner">
      <span></span>
      <span></span>
      <span></span>
      <h2>devbw.</h2>
    </div>
    <h1>Qui suis-je ?</h1>
    <p>Je m'appelle Brian, je suis un explorateur du développement web, des blockchains et des technologies. Mon quotidien est fait de découverte du monde numérique, que ce soit le développement web, la blockchain, les NFT's, les métaverses, la réalité virtuelle ou encore la réalité augmentée.</p>
    <div>
      <i class="fab fa-github" @click="openGit()"></i>
      <i class="fab fa-linkedin" @click="openLk()"></i>
    </div>
  </div>
</template>

<script>

export default {
  name: 'About',
  methods: {
    openGit(){
      window.open("https://github.com/devbw");
    },
    openLk(){
      window.open("https://www.linkedin.com/in/brianwullaertdev/");
    },
  }
}
</script>

<style scoped>
h1{
  margin-top: 6rem;
}
h2{
  color: white;
  font-size: 2rem;
}
p{
  width: 50%;
  text-align: center;
}
.sontainer{
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 8rem 0 6rem 0;
}
.fab{
  font-size: 2rem;
  margin: 2rem 1.5rem;
  cursor: pointer;
  transition: .5s;
}
.fab:hover{
  transform: rotate(90deg);
  color: #bd3bb6;
}
.socials{
  display: flex;
}
</style>