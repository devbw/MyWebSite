<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300&display=swap");

#app {
  font-family: "Poppins", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background: var(--linear);
  color: #fff;
}
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.background {
  background: #1d2026;
  min-height: 100vh;
  max-height: 100%;
  padding: 1rem;
}
.fade-in-bottom {
  -webkit-animation: fade-in-bottom 1s cubic-bezier(0.39, 0.575, 0.565, 1) both;
  animation: fade-in-bottom 1s cubic-bezier(0.39, 0.575, 0.565, 1) both;
}
@-webkit-keyframes fade-in-bottom {
  0% {
    -webkit-transform: translateY(50px);
    transform: translateY(50px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    opacity: 1;
  }
}
@keyframes fade-in-bottom {
  0% {
    -webkit-transform: translateY(50px);
    transform: translateY(50px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    opacity: 1;
  }
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
  animation: animate 10s linear infinite;
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
