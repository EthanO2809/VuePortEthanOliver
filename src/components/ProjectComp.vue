<template>
  <div>
    <div class="container">
      <div class="row">
        <div
          class="col-6 mb-5 mt-5 con"
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
                    <a :href="item.github" style="margin-right: 1rem;" class="btn btn-primary" target="_blank">Github</a>
                    <a :href="item.netlify" class="btn btn-primary" target="_blank">Netlify</a>
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
a {
  position: relative;
  width: 7em;
  height: 2.5em;
  border-radius: 1em;
  text-align: center;
  font-family: poppins;
  font-size: 14px;
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

a:focus,
a:hover {
  box-shadow: 0 0 110px #fff;
  background-color: rgba(255, 255, 255, 0.4);
  color: #111;
  font-weight: 500;
}

a:focus:before,
a:hover:before,
a:focus:after,
a:hover:after {
  width: 100%;
  left: 0%;
}

a:before,
a:after {
  content: '';
  position: absolute;
  pointer-events: none;
  left: 50%;
  width: 0%;
  height: 2px;
  background-color: #fff;
  transition: width, left, 250ms cubic-bezier(0.25, .8, .25, 1);
}

a:before {
  top: -2px;
}

a:after {
  bottom: -2px;
}

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
  border-radius: 15px;
}

.card .front-content {
  width: 100%;
  height: 100%;
 border-radius: 15px;
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

@media (width <= 300px) {
  .card-container {
    width: 250px;
    height: 250px;
    margin: 0 !important;
    font-size: 10px;
  }
  .card {
    width: 250px;
    margin: 0 !important;
    height: 250px;
    font-size: 10px !important;
  }
  .row {
    display: flex !important;
    flex-direction: column;
    justify-content: center !important;
    align-items: center !important;
  }
  .con {
    display: flex !important;
    flex-direction: column;
    justify-content: center !important;
    align-items: center !important;
  }
  .hvr {
    width: 250px !important;
    height: 250px !important;
  }
  .heading {
    font-size: 14px !important;
    margin-bottom: 3rem;
  }
  .btn {
    width: 4rem;
    height: 1rem;
    font-size: 6px !important;
  }
}
@media (width <= 700px) {
  .card-container {
    width: 250px;
    height: 250px;
    margin: 0 !important;
    font-size: 10px;
  }
  .card {
    width: 250px;
    margin: 0 !important;
    height: 250px;
    font-size: 10px !important;
  }
  .row {
    display: flex !important;
    flex-direction: column;
    justify-content: center !important;
    align-items: center !important;
  }
  .con {
    display: flex !important;
    flex-direction: column;
    justify-content: center !important;
    align-items: center !important;
  }
  .hvr {
    width: 250px !important;
    height: 250px !important;
  }
  .heading {
    font-size: 14px !important;
    margin-bottom: 3rem;
  }
  .btn {
    width: 4rem;
    height: 1rem;
    font-size: 6px !important;
  }
}
</style>
