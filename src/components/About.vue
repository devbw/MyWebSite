<template>
  <div class="container">
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
.container{
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 8rem 0 6rem 0;
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