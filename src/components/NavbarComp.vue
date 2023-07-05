<template>
  <div>
    <nav class="navbar navbar-expand-lg">
      <div class="container-fluid">
        <a class="navbar-brand text-white h-02" href="#">Ethan Oliver <br> Web Developer</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav ms-auto mb-2 mb-lg-">
            <li class="nav-item">
              <router-link to="/" class="text-decoration-none">Home</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/about" class="text-decoration-none">About</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/resume" class="text-decoration-none">Resume</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/projects" class="text-decoration-none">Projects</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/testimonials" class="text-decoration-none">Testimonial</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/contact" class="text-decoration-none">Contact</router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
  export default {
    
  }
</script>

<style scoped>
.nav-item {
  color: white;
  text-decoration: none;
  font-size: 25px;
  border: none;
  background: none;
  font-family: 'LOVES', sans-serif;
}

.h-02 {
  font-family: 'LOVES', sans-serif;
}

@import url('https://fonts.cdnfonts.com/css/loves');

.nav-item::before {
  margin-left: auto;
}

.nav-item::after, .nav-item::before {
  content: '';
  width: 0%;
  height: 2px;
  background: #ffffff;
  display: block;
  transition: 0.5s;
}

.nav-item:hover::after, .nav-item:hover::before {
  width: 100%;
}
</style>