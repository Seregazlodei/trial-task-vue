<template>
  <div id="app">
    <Navbar />
    <router-view/>
  </div>
</template>

<script>
  import Navbar from '@/components/Navbar.vue'
  export default {
    components: {Navbar}
  }
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 60px auto;
  width: 400px;
}

.post {
  border: 1px solid #ccc;
  border-radius: 5px;
  margin-bottom: 1rem;
}
</style>
