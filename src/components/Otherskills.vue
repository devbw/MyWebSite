<template>
  <div class="container__skills">
    <div class="skills">
      <div class="spinner">
        <div class="skill">
          <span class="one"></span>
          <span class="two"></span>
          <div class="skill__info">
            <i class="fab fa-gitlab"></i>
            <p>Gitlab</p>
          </div>
        </div>
      </div>
      <div class="spinner">
        <div class="skill">
          <span class="three"></span>
          <span class="four"></span>
          <div class="skill__info">
            <i class="fab fa-git-alt"></i>
            <p>Git</p>
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
            <i class="fab fa-linux"></i>
            <p>Linux</p>
          </div>
        </div>
      </div>
      <div class="spinner">
        <div class="skill">
          <span class="seven"></span>
          <span class="eight"></span>
          <div class="skill__info">
            <i class="fab fa-windows"></i>
            <p>Windows</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Otherskills',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h2, h3, p{
  color: white;
}
p{
  margin: .1rem;
}
.container__skills{
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 3rem;
}
.spinner{
  position: relative;
  width: 100px;
  height: 100px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 1rem;
}
.spinner span{
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: 2px solid white;
  pointer-events: none;
  animation: animate 2s linear infinite;
}
.spinner .one{
  border-radius: 30% 70% 70% 30% / 30% 30% 70% 70% ;
  border-color: #E2432A;
}
.spinner .two{
  animation-direction: reverse;
  border-radius: 74% 26% 42% 58% / 62% 65% 35% 38% ;
  border-color: #FCA326;
  animation-duration: 6s;
}
.spinner .three{
  animation-duration: 5s;
  border-radius: 49% 51% 26% 74% / 27% 29% 71% 73% ;
  border-color: #F1502F;
  animation-direction: reverse;
}
.spinner .four{
  animation-duration: 3s;
  border-radius: 74% 26% 42% 58% / 62% 65% 35% 38% ;
  border-color: #3E2C00;
}
.spinner .five{
  animation-duration: 3s;
  border-radius: 49% 51% 26% 74% / 27% 29% 71% 73% ;
  border-color: #FFF;
}
.spinner .six{
  animation-duration: 2s;
  animation-direction: reverse;
  border-radius: 74% 26% 42% 58% / 62% 65% 35% 38% ;
  border-color: #FCA326;
}
.spinner .seven{
  animation-duration: 3s;
  border-radius: 49% 51% 26% 74% / 27% 29% 71% 73% ;
  border-color: #7FBA00;
}
.spinner .eight{
  animation-duration: 2.5s;
  border-radius: 30% 70% 70% 30% / 30% 30% 70% 70% ;
  border-color: #00A4EF;
  animation-direction: reverse;
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
.fab{
  color: white;
  font-size: 1.5rem;
}
.skill__info{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.skills{
  display: flex;
  justify-content: center;
}
</style>
