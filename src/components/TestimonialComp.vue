<template>
  <div>
    <div class="container">
      <h4 class="text-center text-white fs-2">Hover Cards</h4>
      <div class="row mt-5 mb-5">
        <div
          class="col-4"
          v-for="item in testimonials"
          :key="item.id"
          data-aos="flip-down"
        >
        <center>
          <div class="card">
            <img
              :src="item.image"
              style="height: 400px; width: 300px"
              class="card-img-top"
              :alt="item.name"
            />
            <div class="card__content">
              <p class="card__title">{{ item.name }}</p>
              <p class="card__title">{{ item.role }}</p>
              <p class="card__description">{{ item.words }}</p>
            </div>
          </div>
          </center>
        </div>
      </div>
    </div>

    <!-- <div class="card mb-5" style="width: 18rem;">
                        <img :src="item.image" style="height: 24rem;" class="card-img-top" :alt="item.name">
                        <div class="card-body">
                          <p class="card-text">{{ item.name }}</p>
                          <p class="card-text">{{ item.role }}</p>
                          <p class="card-text">{{ item.words }}</p>
                        </div>
    </div> -->
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
  position: relative;
  width: 300px;
  height: 400px;
  background: linear-gradient(-45deg, #296bf8 0%, #0fefff 100%);
  border-radius: 10px;
  margin-bottom: 6rem;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
  perspective: 1000px;
  box-shadow: 0 0 0 5px #ffffff80;
  transition: all 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}

.card svg {
  width: 48px;
  fill: #333;
  transition: all 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}

.card:hover {
  transform: scale(1.05);
  box-shadow: 0 8px 16px rgba(255, 255, 255, 0.2);
}

.card__content {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  padding: 20px;
  box-sizing: border-box;
  background: linear-gradient(-45deg, #296bf8 0%, #0fefff 100%);
  transform: rotateX(-90deg);
  transform-origin: bottom;
  transition: all 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}

.card:hover .card__content {
  transform: rotateX(0deg);
}

.card__title {
  margin: 0;
  font-size: 24px;
  color: #333;
  font-weight: 700;
}

.card:hover svg {
  scale: 0;
}

.card__description {
  margin: 10px 0 0;
  font-size: 14px;
  color: #777;
  line-height: 1.4;
}
</style>
