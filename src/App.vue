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

</style>
