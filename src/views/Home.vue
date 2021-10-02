<template>
  <div class="background">
    <Menu />
    <About />
  </div>
</template>

<script>
import Menu from '@/components/Menu.vue'
import About from '@/components/About.vue'

export default {
  name: 'Home',
  components: {
    Menu,
    About,
  }
}
</script>

<style scoped>
.background{
  background: #1d2026;
  min-height: 100vh;
  max-height: 100%;
  padding: 1rem;
}
</style>