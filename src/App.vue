<template>
  <Navbar/>
  <router-view/>
  <Footer/>
</template>

<script>
import Navbar from './components/NavbarComp.vue'
import Footer from './components/FooterComp.vue'
export default {
  components: {
    Navbar,
    Footer
  }
}
</script>

<style>
#app {
  font-family: 'D-DIN Exp', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

@import url('https://fonts.cdnfonts.com/css/d-din');
@import url('https://fonts.cdnfonts.com/css/loves');

nav {
  padding: 30px;
  color: white;
}

nav a {
  font-weight: bold;
  color: #ffffff;
  margin: .8rem;
}

body {
  background: linear-gradient(to right, #3CC4FF, #3CC4FF, #000000);
  background-attachment: fixed;
}

</style>
