<template>
    <div class="container">
        <div class="row mt-3">
            <div class="col-6 one">
                <img src="https://i.postimg.cc/6QNHJQyn/IMG-9863-1.jpg" alt="" class="img-01 mb-3">
                <div class="text-white lft">
                <p class="fnt-s">Full Name : Ethan Liam Oliver</p>
                <p class="fnt-s">Age : 21</p>
                <p class="fnt-s">Email Address : example@gmail.com</p>
                <p class="fnt-s">Contact No. : +27 11 222 3333</p>
                <p class="fnt-s">Willing To Relocate : Yes</p>
                <p class="fnt-s">Employment Status : Unemployed</p>
                <p class="fnt-s">Marital Status : Single</p>
                <a href="https://drive.google.com/file/d/1t0BnbXGb5EIiBsv8U6aEOf3tNCeaW5vp/view?usp=sharing" target="_blank"><button>
                    View My CV Here
                </button></a>
                </div>
            </div>
            <div class="col-6">
                <h4 class="text-white txt1"><u>About Me</u></h4>
                <p class="text-white txt2 mt-4">While studying IT, I started learning <br> graphic design and web design. After <br> graduating, I started my coding career <br> with Life Choices Academy. Moving <br> on, I built practice e-commerce sites, <br> developed design skills, and recently <br> started developing websites for <br> companies. I learned so much from the <br> amazing Academy I’m working with. <br> Now, I want to help other brands stand <br> out in the big industry.</p>
                <hr class="hr-01">
                <router-link to="/projects" class="text-decoration-none">
                <button>
                    View My Projects
                </button>
                </router-link>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
.img-01 {
    border-radius: 2rem;
    display: flex;
    width: 8rem !important;
}

.txt1 {
    font-size: 2rem !important;
}

.txt2 {
    font-size: 1.5rem !important;
}

.lft{
    text-align: left;
}

.one {
    border-right: white solid;
}

.hr-01 {
    border: white solid 2px;
}

button {
  position: relative;
  width: 16em !important;
  height: 6em !important;
  border-radius: 1em;
  text-align: center;
  font-family: poppins;
  font-size: .5rem !important;
  font-weight: 700;
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

.fnt-s{
    font-size: 1.2rem !important;
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

@media (width <= 300px) {
  .fnt-s {
    font-size: 10px !important;
  }
  .txt1{
    font-size: 16px !important;
  }
  .txt2 {
    font-size: 10px !important;
  }
  button {
    width: 6rem !important;
    height: 2rem !important;
    font-size: 8px !important;
  }
  .img-01 {
    width: 4rem !important;
    border-radius: 1rem !important;
  }
}
@media (width <= 700px) {
  .fnt-s {
    font-size: 10px !important;
  }
  .txt1{
    font-size: 16px !important;
  }
  .txt2 {
    font-size: 10px !important;
  }
  button {
    width: 6rem !important;
    height: 2rem !important;
    font-size: 8px !important;
  }
  .img-01 {
    width: 4rem !important;
    border-radius: 1rem !important;
  }
}
</style>