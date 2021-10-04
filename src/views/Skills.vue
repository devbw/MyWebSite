<template>
  <div class="background">
    <Menu />
    <div class="container">
      <h1>Skills</h1>
      <p>Que ce soit du front, du back ou de la base de donnée, découvrez les différentes technologies avec lesquelles je travaille au quotidien !</p>
    </div>
    <div class="skills">
      <div class="skill">
        <h3 @click="showFront()">Front</h3>
        <h3 @click="showBack()">Back</h3>
        <h3 @click="showOthers()">Others</h3>
      </div>
    </div>
    <Front v-if="front"/>
    <Back v-if="back"/>
    <Others v-if="others"/>
  </div>
</template>

<script>
import Menu from '@/components/Menu.vue'
import Front from '@/components/Frontskills.vue'
import Back from '@/components/Skillsback.vue'
import Others from '@/components/Otherskills.vue'

export default {
  name: 'Skills',
  data() {
    return {
      front: true,
      back: false,
      others: false,
    }
  },
  components: {
    Menu,
    Front,
    Back,
    Others
  },
  methods: {
    showBack() {
      this.front = false;
      this.back = true;
      this.others = false;
    },
    showFront() {
      this.front = true;
      this.back = false;
      this.others = false;
    },
    showOthers() {
      this.front = false;
      this.back = false;
      this.others = true;
    }
  }
};
</script>

<style>
h1 {
  margin: 1rem;
}
.container {
  width: 90%;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 10rem auto 1rem auto;
  text-align: center;
}
.skills{
  width: 100%;
}
.skill{
  display: flex;
  justify-content: center;
  margin: 4rem 0;
}
.skill h3{
  margin: 0 1rem;
  cursor: pointer;
}
</style>
