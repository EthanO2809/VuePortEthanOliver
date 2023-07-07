<template>
  <div>
    <hr class="hr-01 mt-5" />
    <h1 class="text-white">Education:</h1>
    <br>
    <div class="container center">
      <div class="row">
        <div class="col" v-for="item in education" :key="item.id" data-aos="zoom-in-up">
          <center>
          <div class="flip">
    <div class="content">
        <div class="front">
           <p> <img
              :src="item.image"
              style="height: 300px; width: 250px;"
              class="card-img-top img-01"
              :alt="item.place"
            />
            </p>
        </div>
        <div class="back">
            <h2> {{ item.place }} </h2>
            <p> {{ item.qualification }} </p>
            <p> Completed : {{ item.year }} </p>
        </div>
    </div>
</div>
</center>
        </div>
      </div>
    </div>
    <br>
    <br>
    <hr class="hr-01" />
    <h1 class="text-white">Softskills:</h1>
    <div class="container mb-5 mt-5">
      <div class="row">
        <div class="col" v-for="item in softskills" :key="item.id" data-aos="zoom-in-up">
          <center>
          <div class="card1">
  <div class="upper-part">
    <div class="upper-part-face"><img :src="item.image" :alt="item.soft" style="width: 100%; height: 100%; border-radius: 1rem;"></div>
    <div class="upper-part-back"><p> {{ item.words }} </p></div>
  </div>
  <div class="lower-part">
    <div class="lower-part-face"> {{ item.soft }} </div>
    <div class="lower-part-back"> {{ item.soft }} </div>
  </div>
</div>
</center>
        </div>
      </div>
    </div>
    <hr class="hr-01" />
    <h1 class="text-white">Hardskills:</h1>
    <div class="container cont mt-5 mb-5 center fs-3">
      <div class="row">
        <div class="col-4 con" v-for="item in hardskills" :key="item.id" data-aos="zoom-in-up">
          <center>
          <div class="card1">
  <div class="upper-part">
    <div class="upper-part-face"><img :src="item.icon" :alt="item.name" style="width: 100%; height: 100%; border-radius: 1rem;"></div>
    <div class="upper-part-back"><p> {{ item.words }} </p></div>
  </div>
  <div class="lower-part">
    <div class="lower-part-face"> {{ item.name }} </div>
    <div class="lower-part-back"> {{ item.name }} </div>
  </div>
</div>
</center>
        </div>
      </div>
    </div>
    <hr class="hr-01" />
    <h1 class="text-white">Experience:</h1>
    <div class="container center mt-5 mb-5">
      <div class="row">
        <div class="col" v-for="item in experience" :key="item.id" data-aos="zoom-in-up">
          <div class="flip1">
    <div class="content">
        <div class="front">
           <p> <img
              :src="item.image"
              style="height: 300px; width: 250px;"
              class="card-img-top"
              :alt="item.place"
            />
            </p>
        </div>
        <div class="back">
            <h2> {{ item.place }} </h2>
            <p> {{ item.role }} </p>
            <p style="font-size: 12px;">{{ item.description }}</p>
            <p style="font-size: 12px;">Year Completed : {{ item.Year }} </p>
        </div>
    </div>
</div>
          <!-- <div class="card" style="width: 18rem">
            <img :src="item.image" class="card-img-top" :alt="item.place" />
            <div class="card-body">
              <p class="card-text fs-3">{{ item.year }}</p>
              <p class="card-text fs-3">{{ item.place }}</p>
              <p class="card-text fs-3">{{ item.role }}</p>
              <p class="card-text">{{ item.description }}</p>
            </div>
          </div> -->
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    education() {
      return this.$store.state.education;
    },
    hardskills() {
      return this.$store.state.hardskills;
    },
    softskills() {
      return this.$store.state.softskills;
    },
    experience() {
      return this.$store.state.experience;
    },
  },
  mounted() {
    this.$store.dispatch("fetchEducation"),
      this.$store.dispatch("fetchHardskills"),
      this.$store.dispatch("fetchSoftskills"),
      this.$store.dispatch("fetchExperience");
  },
};
</script>

<style scoped>
.center {
  display: flex;
  justify-content: center;
  align-content: center;
}

.space {
  margin: 2rem;
}

.card-01 {
  width: rem;
}

.hvr:hover {
  background-color: rgb(100, 185, 255);
  font-weight: 800;
  border-radius: 0.3rem;
  color: white;
}

.hr-01 {
  border: white solid 1px;
}

.bck {
    background-color: rgba(0, 0, 0, 0);
    border: rgba(0, 0, 0, 0) solid;
}

.bck:hover {
    transform: scale(1.1);
    transition: ease-in .5s;
}

.txt {
    color: black;
} 
.flip {
  box-shadow: 0 10px 20px rgb(0, 0, 0);
  width: 250px;
  height: 300px;
  transform-style: preserve-3d;
  transition: 1s ease;
}

.flip:hover {
  transform: rotateY(180deg);
}
/* Content */
.flip .content {
  transform-style: preserve-3d;
}

.flip .back, .flip .front {
  transform-style: preserve-3d;
  backface-visibility: hidden;
  display: flex;
  flex-direction: column;
}

.flip .back {
  transform: rotateY(180deg);
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
}

.flip h2,
.flip p {
  transform: translateZ(90px);
  text-shadow: 0 0 3px black;
  text-align: center;
}

.flip h2 {
  font-size: 3em;
  color: #fff;
  letter-spacing: 1px;
}

.flip p {
  font-size: 1em;
  color: #eee;
  line-height: 1.6em;
}

.flip::before,
.flip::after {
  content: "";
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  position: absolute;
  background: linear-gradient(-45deg, #296bf8 0%, #005f65 100%);
  background-position: center center;
  background-repeat: no-repeat;
  background-size: cover;
  transform: rotateY(180deg)translateZ(1px);
}

.flip::before {
  transform: none;
  background: linear-gradient(-45deg, #296bf8 0%, #005f65 100%);
  background-position: center center;
  background-repeat: no-repeat;
  background-size: cover;
}

.flip1 {
  box-shadow: 0 0 26px 6px rgb(0, 0, 0);
  width: 250px;
  height: 300px;
  transform-style: preserve-3d;
  transition: 1s ease;
}

.flip1:hover {
  transform: rotateY(180deg);
}
/* Content */
.flip1 .content {
  transform-style: preserve-3d;
}

.flip1 .back, .flip1 .front {
  transform-style: preserve-3d;
  backface-visibility: hidden;
  display: flex;
  flex-direction: column;
}

.flip1 .back {
  transform: rotateY(180deg);
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
}

.flip1 h2,
.flip1 p {
  transform: translateZ(90px);
  text-shadow: 0 0 3px black;
  text-align: center;
}

.flip1 h2 {
  font-size: 3em;
  color: #fff;
  letter-spacing: 1px;
}

.flip1 p {
  font-size: 1em;
  color: #eee;
  line-height: 1.6em;
}

.flip1::before,
.flip1::after {
  content: "";
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  position: absolute;
  background: linear-gradient(-45deg, #296bf8 0%, #005f65 100%);
  background-position: center center;
  background-repeat: no-repeat;
  background-size: cover;
  transform: rotateY(180deg)translateZ(1px);
}

.flip1::before {
  transform: none;
  background: linear-gradient(-45deg, #296bf8 0%, #005f65 100%);
  background-position: center center;
  background-repeat: no-repeat;
  background-size: cover;
}

.card1 {
  width: 190px;
  height: 254px;
  margin-bottom: 4rem;
  box-shadow: #000000 0px 2px 8px 4px;
  position: relative;
  border-radius: 40px;
  transition: all 0.8s;
  perspective: 600px;
  perspective-origin: center bottom;
}

.upper-part {
  width: 100%;
  height: 65%;
  border-radius: 40px 40px 0 0;
  position: relative;
  transform-style: preserve-3d;
  transition: all 0.9s;
}

.upper-part-face,
.upper-part-back {
  text-align: center;
  background: linear-gradient(-45deg, #296bf8 0%, #005f65 100%);
  color: purple;
  border: 3px solid rgb(19, 0, 128);
  display: flex;
  font-size: 14px;
  justify-content: center;
  align-items: center;
  position: absolute;
  width: 100%;
  height: 100%;
  padding: 15px;
  border-radius: 40px 40px 0 0;
  font-weight: bold;
  z-index: 2;
  backface-visibility: hidden;
  transition: all 0.6s;
}

.upper-part-back {
  background: linear-gradient(-45deg, #296bf8 0%, #005f65 100%);
  color: lightgray;
  transform: rotatex(180deg);
}

.lower-part {
  width: 100%;
  height: 35%;
  border-radius: 0 0 40px 40px;
  position: relative;
  transform-style: preserve-3d;
  transform-origin: center top;
  transition: all 0.9s;
}

.lower-part-face,
.lower-part-back {
  background: linear-gradient(-45deg, #296bf8 0%, #000000 100%);
  width: 100%;
  height: 100%;
  color: rgb(255, 255, 255);
  font-weight: bold;
  position: absolute;
  border-radius: 0 0 40px 40px;
  display: flex;
  justify-content: center;
  align-items: center;
  transform: translate(0, -0.8px);
  backface-visibility: hidden;
  z-index: 2;
}

.lower-part-back {
  backface-visibility: visible;
  border-radius: 40px;
  color: rgb(255, 255, 255);
  background-color: lightgray;
  transform: rotateX(180deg);
  z-index: 1;
  transition: border-radius 0.6s;
}

.card1:hover > .upper-part {
  transform: rotatex(-0.5turn);
}

.card1:hover > .lower-part {
  transform: translateY(88.3px) rotateX(0.5turn);
}

.card1:hover > .lower-part > .lower-part-back {
  border: 3px solid rgb(25, 0, 255);
  border-radius: 0 0 40px 40px;
}

@media (width <= 300px) {
  .flip {
    width: 200px !important;
    height: 200px !important;
    margin-bottom: 1rem!important;
  }
  .flip p {
    font-size: 16px !important;
  }
  .flip h2 {
    font-size: 18px;
    margin-top: 1rem;
  }
  .img-01 {
    width: 200px !important;
    height: 200px !important;
  }
  .row {
    display: flex !important;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .con {
    display: flex !important;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
}
@media (width <= 700px) {
  .flip {
    width: 200px !important;
    height: 200px !important;
    margin-bottom: 1rem!important;
  }
  .flip p {
    font-size: 16px !important;
  }
  .flip h2 {
    font-size: 18px;
    margin-top: 1rem;
  }
  .img-01 {
    width: 200px !important;
    height: 200px !important;
  }
  .row {
    display: flex !important;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .con {
    display: flex !important;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
}
</style>
