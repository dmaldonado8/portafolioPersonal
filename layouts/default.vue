<template>
  <div>
    <Navbar/>
    <nuxt />
  </div>
</template>

<script>
import Navbar from '~/components/Navbar.vue';
export default {
  components: {
    Navbar
  }
}
</script>


<style lang="scss">
@import '../assets/variables';
@import url('https://fonts.googleapis.com/css?family=Raleway&display=swap');

html {
  font-family: 'Raleway', sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: content-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  height: 100%;
  width: 100%;
}

li {
  list-style: none;
}

a {
  text-decoration: none;
  color: black;
  text-transform: uppercase;
}
</style>
