<template>
  <div class="containerr">
    <div class="about">
      <Card />
    </div>
  </div>
  <router-view></router-view>
</template>

<script>
import Card from '../components/Card.vue'

export default {
  name: 'Dictionary',
  components: {
    Card,
  },
  data() {
    return {}
  },
}
</script>

<style scoped>
.containerr {
  height: 100vh;
  display: flex;
  justify-content: center;
  flex-direction: column;
  margin: 0 auto;
  width: 50%;
  min-width: 400px;
}
</style>
