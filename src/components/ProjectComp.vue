<template>
  <div>
    <div class="container">
      <div class="row">
        <div
          class="col-6 mb-5 mt-5"
          v-for="item in projects"
          :key="item.id"
          data-aos="fade-up"
          data-aos-duration="3000"
        >
          <center>
            <div class="card-container">
              <div class="card">
                <div class="front-content">
                  <p>
                    <img
                      :src="item.image"
                      style="height: 400px; width: 550px"
                      class="card-img-top hvr"
                      :alt="item.name"
                    />
                  </p>
                </div>
                <div class="content">
                  <p class="heading">{{ item.name }}</p>
                  <p>
                    {{ item.description }}
                    <br />
                    <br />
                    <a :href="item.github" class="btn btn-primary">Github</a>
                    <br />
                    <br />
                    <a :href="item.netlify" class="btn btn-primary">Netlify</a>
                  </p>
                </div>
              </div>
            </div>
          </center>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    projects() {
      return this.$store.state.projects;
    },
  },
  mounted() {
    this.$store.dispatch("fetchProjects");
  },
};
</script>

<style scoped>
.card-container {
  width: 550px;
  height: 400px;
  position: relative;
  border-radius: 10px;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
  overflow: hidden;
}

.card {
  width: 100%;
  height: 100%;
  border-radius: inherit;
}

.card .front-content {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.6s cubic-bezier(0.23, 1, 0.32, 1);
}

.card .front-content p {
  font-size: 32px;
  font-weight: 700;
  opacity: 1;
  background: linear-gradient(-45deg, #296bf8 0%, #0fefff 100%);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  transition: all 0.6s cubic-bezier(0.23, 1, 0.32, 1);
}

.card .content {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  gap: 10px;
  background: linear-gradient(-45deg, #296bf8 0%, #003235 100%);
  color: #e8e8e8;
  padding: 20px;
  line-height: 1.5;
  border-radius: 5px;
  pointer-events: none;
  transform: translateY(96%);
  transition: all 0.6s cubic-bezier(0.23, 1, 0.32, 1);
}

.card .content .heading {
  font-size: 32px;
  font-weight: 700;
}

.card:hover .content {
  transform: translateY(0);
}

.card:hover .front-content {
  transform: translateY(-30%);
}

.card:hover .front-content p {
  opacity: 0;
}
</style>
