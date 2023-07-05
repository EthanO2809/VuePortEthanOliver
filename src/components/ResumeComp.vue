<template>
  <div>
    <hr class="hr-01 mt-5" />
    <h1 class="text-white">Education:</h1>
    <div class="container center">
      <div class="row">
        <div class="col" v-for="item in education" :key="item.id">
          <div class="card space" style="width: 18rem; height: 24rem">
            <img
              :src="item.image"
              style="height: 16rem"
              class="card-img-top card-01"
              :alt="item.place"
            />
            <div class="card-body">
              <p class="card-text">{{ item.place }}</p>
              <p class="card-text">{{ item.qualification }}</p>
              <p class="card-text">{{ item.year }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <hr class="hr-01" />
    <h1 class="text-white">Softskills:</h1>
    <div class="container mb-5 mt-5">
      <div class="row">
        <div class="col" v-for="item in softskills" :key="item.id">
          <div class="card">
            <div class="card-body hvr">
              {{ item.soft }}
            </div>
          </div>
        </div>
      </div>
    </div>
    <hr class="hr-01" />
    <h1 class="text-white">Hardskills:</h1>
    <div class="container mt-5 mb-5 center fs-3">
      <div class="row">
        <div class="col-4" v-for="item in hardskills" :key="item.id">
          <div class="card mb-5 bck" style="width: 18rem">
            <p class="card-text txt">{{ item.name }}</p>
            <div class="card-body">
              <img :src="item.icon" class="card-img-top bck" :alt="item.name" />
            </div>
          </div>
        </div>
      </div>
    </div>
    <hr class="hr-01" />
    <h1 class="text-white">Experience:</h1>
    <div class="container center mt-5 mb-5">
      <div class="row">
        <div class="col" v-for="item in experience" :key="item.id">
          <div class="card" style="width: 18rem">
            <img :src="item.image" class="card-img-top" :alt="item.place" />
            <div class="card-body">
              <p class="card-text fs-3">{{ item.year }}</p>
              <p class="card-text fs-3">{{ item.place }}</p>
              <p class="card-text fs-3">{{ item.role }}</p>
              <p class="card-text">{{ item.description }}</p>
            </div>
          </div>
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
</style>
