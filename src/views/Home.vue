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

</style>