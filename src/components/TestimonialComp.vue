<template>
  <div>
    <div class="container">
      <h4 class="text-center text-white fs-2">Hover Cards</h4>
      <div class="row mt-5 mb-5">
        <div
          class="col-4 con"
          v-for="item in testimonials"
          :key="item.id"
          data-aos="flip-down"
        >
        <center>
          <div class="card">
            <img
              :src="item.image"
              style="height: 400px; width: 300px"
              class="card-img-top img-01"
              :alt="item.name"
            />
            <div class="card__content">
              <p class="card__title text-white">{{ item.name }}</p>
              <p class="card__title text-white">{{ item.role }}</p>
              <p class="card__description fs-6 text-white">{{ item.words }}</p>
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
    testimonials() {
      return this.$store.state.testimonials;
    },
  },
  mounted() {
    this.$store.dispatch("fetchTestimonials");
  },
};
</script>

<style scoped>
.card {
  position: relative !important;
  width: 300px!important;
  height: 400px!important;
  background: linear-gradient(-45deg, #296bf8 0%, #0fefff 100%)!important;
  border-radius: 10px!important;
  margin-bottom: 6rem!important;
  display: flex!important;
  align-items: center!important;
  justify-content: center!important;
  overflow: hidden!important;
  perspective: 1000px!important;
  box-shadow: 0 0 0 5px #ffffff80!important;
  transition: all 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275)!important;
}

.card svg {
  width: 48px!important;
  fill: #333!important;
  transition: all 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275)!important;
}

.card:hover {
  transform: scale(1.05)!important;
  box-shadow: 0 8px 16px rgba(255, 255, 255, 0.2)!important;
}

.card__content {
  position: absolute!important;
  top: 0!important;
  left: 0!important;
  width: 100%!important;
  height: 100%!important;
  padding: 20px!important;
  box-sizing: border-box!important;
  background: linear-gradient(-45deg, #296bf8 0%, #0fefff 100%)!important;
  transform: rotateX(-90deg)!important;
  transform-origin: bottom!important;
  transition: all 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275)!important;
}

.card:hover .card__content {
  transform: rotateX(0deg)!important;
}

.card__title {
  margin: 0!important;
  font-size: 24px!important;
  color: #333!important;
  font-weight: 700!important;
}

.card:hover svg {
  scale: 0!important;
}

.card__description {
  margin: 10px 0 0!important;
  font-size: 14px!important;
  color: #777!important;
  line-height: 1.4!important;
}

@media (width <= 300px) {
  .card {
    width: 200px !important;
    height: 250px !important;
    margin-top: 4rem;
    margin-bottom: 8rem!important;
  }
  .card p {
    font-size: 10px !important;
  }
  .flip h2 {
    font-size: 18px;
    margin-top: 1rem;
  }
  .img-01 {
    width: 200px !important;
    height: 250px !important;
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
  .card {
    width: 200px !important;
    height: 250px !important;
    margin-top: 4rem;
    margin-bottom: 8rem!important;
  }
  .card p {
    font-size: 10px !important;
  }
  .flip h2 {
    font-size: 18px;
    margin-top: 1rem;
  }
  .img-01 {
    width: 200px !important;
    height: 250px !important;
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
