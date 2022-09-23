<template>
  <Navbar />
</template>

<script>
import Navbar from './components/Navbar.vue'

export default {
  name: 'App',
  components: {
    Navbar
  }
}
</script>

<style>
* {
  font-family: 'Ubuntu', sans-serif;
  list-style-type: none;
  text-decoration: none;
  margin: 0;
  padding: 0;
}
</style>
