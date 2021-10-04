<template>
  <div class="container__skills">
    <div class="skills">
      <div class="spinner">
        <div class="skill">
          <span class="one"></span>
          <span class="two"></span>
          <div class="skill__info">
            <i class="fab fa-html5"></i>
            <p>HTML</p>
          </div>
        </div>
      </div>
      <div class="spinner">
        <div class="skill">
          <span class="three"></span>
          <span class="four"></span>
          <div class="skill__info">
            <i class="fab fa-css3-alt"></i>
            <p>CSS</p>
          </div>
        </div>
      </div>
    </div>
    <div class="skills">
      <div class="spinner">
        <div class="skill">
          <span class="five"></span>
          <span class="six"></span>
          <div class="skill__info">
            <i class="fab fa-js"></i>
            <p>JS</p>
          </div>
        </div>
      </div>
      <div class="spinner">
        <div class="skill">
          <span class="seven"></span>
          <span class="eight"></span>
          <div class="skill__info">
            <i class="fab fa-vuejs"></i>
            <p>Vue.js</p>
          </div>
        </div>
      </div>
    </div>
    <div class="skills">
      <div class="spinner">
        <div class="skill">
          <span class="nine"></span>
          <span class="ten"></span>
          <div class="skill__info">
            <i class="fab fa-react"></i>
            <p>ReactJS</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Frontskills',
};
</script>

<style scoped>
h2,
h3,
p {
  color: white;
}
p {
  margin: 0.1rem;
}
.container__skills {
  margin-bottom: 3rem;
}
.spinner {
  position: relative;
  width: 100px;
  height: 100px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 1rem;
}
.spinner span {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: 2px solid white;
  pointer-events: none;
  animation: animate 2s linear infinite;
}
.spinner .one {
  border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
  border-color: #c70039;
}
.spinner .two {
  animation-direction: reverse;
  border-radius: 74% 26% 42% 58% / 62% 65% 35% 38%;
  border-color: #ff5733;
  animation-duration: 6s;
}
.spinner .three {
  animation-duration: 5s;
  border-radius: 49% 51% 26% 74% / 27% 29% 71% 73%;
  border-color: #66d3fa;
  animation-direction: reverse;
}
.spinner .four {
  animation-duration: 3s;
  border-radius: 74% 26% 42% 58% / 62% 65% 35% 38%;
  border-color: #3c99dc;
}
.spinner .five {
  animation-duration: 3s;
  border-radius: 49% 51% 26% 74% / 27% 29% 71% 73%;
  border-color: #f0db4f;
}
.spinner .six {
  animation-duration: 2s;
  animation-direction: reverse;
  border-radius: 74% 26% 42% 58% / 62% 65% 35% 38%;
  border-color: #e7962b;
}
.spinner .seven {
  animation-duration: 3s;
  border-radius: 49% 51% 26% 74% / 27% 29% 71% 73%;
  border-color: #41b883;
}
.spinner .eight {
  animation-duration: 2.5s;
  border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
  border-color: #34495e;
  animation-direction: reverse;
}
.spinner .nine {
  animation-duration: 5s;
  border-radius: 49% 51% 26% 74% / 27% 29% 71% 73%;
  border-color: #61DBFB;
  animation-direction: reverse;
}
.spinner .ten {
  animation-duration: 3s;
  border-radius: 74% 26% 42% 58% / 62% 65% 35% 38%;
  border-color: #3c99dc;
}
@keyframes animate {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
.fab {
  color: white;
  font-size: 1.5rem;
}
.skill__info {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.skills {
  display: flex;
  justify-content: center;
}
</style>
