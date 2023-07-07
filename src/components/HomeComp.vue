<template>
  <div class="hgt">
    <div>
      <img
        src="https://i.postimg.cc/qB1tKZr3/emojipng-com-12280844.png"
        alt=""
        class="mt-5 imgs"
      />
      <p class="text-white mt-3 txt">
        Welcome To My Portfolio <br />
        All About Myself And My Skills!
      </p>
      <p class="text-white mt-3 txt fw-lighter">
        I am a Full Stack Web Developer Who Enjoys <br> Time With Designing CSS &
        JavaScript Based Applications.
      </p>
    </div>
    <router-link to="/about" class="text-decoration-none">
      <button>
        Get To Know Me
      </button>
    </router-link>
  </div>
</template>

<script>
export default {

};
</script>

<style scoped>
.hgt {
  height: 66vh;
  font-family: 'LOVES', sans-serif;
  font-weight: 900;
}

.txt {
  font-size: 2rem !important;
}

.imgs {
  width: 6rem !important;
}

button {
  position: relative;
  width: 12em !important;
  height: 4em;
  border-radius: 1em;
  text-align: center;
  font-family: poppins;
  font-size: 14px;
  font-weight: 300;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: #fff;
  cursor: pointer;
  background-color: rgb(83, 109, 255);
  border: none;
  transition: color .2s linear,
        box-shadow .3s linear,
        background-color .3s cubic-bezier(0.25, 0.8, 0.25, 1);
}

button:focus,
button:hover {
  box-shadow: 0 0 110px #fff;
  background-color: rgba(255, 255, 255, 0.4);
  color: #111;
  font-weight: 500;
}

button:focus:before,
button:hover:before,
button:focus:after,
button:hover:after {
  width: 100%;
  left: 0%;
}

button:before,
button:after {
  content: '';
  position: absolute;
  pointer-events: none;
  left: 50%;
  width: 0%;
  height: 2px;
  background-color: #fff;
  transition: width, left, 250ms cubic-bezier(0.25, .8, .25, 1);
}

button:before {
  top: -2px;
}

button:after {
  bottom: -2px;
}

@import url('https://fonts.cdnfonts.com/css/loves');

@media (width <= 300px) {
  .txt {
    font-size: 18px !important;
  }  
  button {
    width: 8rem !important;
  }
  .imgs {
    width: 4rem !important;
  }
}
@media (width <= 700px) {
  .txt {
    font-size: 18px !important;
  }  
  button {
    width: 8rem !important;
  }
  .imgs {
    width: 4rem !important;
  }
}
</style>
