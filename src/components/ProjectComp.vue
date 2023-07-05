<template>
    <div>
        <div class="container">
            <div class="row">
                <div class="col-4 mb-5 mt-5" v-for="item in projects" :key="item.id">
                    <div class="card" style="width: 20rem;">
                        <img :src="item.image" class="card-img-top hvr" :alt="item.name">
                        <div class="card-body">
                          <h5 class="card-title text-body-emphasis">{{ item.name }}</h5>
                          <p class="card-text">{{ item.description }}</p>
                          <a :href="item.github" class="btn btn-primary">Github</a>
                          <a :href="item.netlify" class="btn btn-primary">Netlify</a>
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
            projects() {
                return this.$store.state.projects
            }
        },
        mounted() {
            this.$store.dispatch('fetchProjects')
        }
    }
</script>

<style scoped>
.hvr {
    height: 12rem;
}

.hvr:hover {
    transform: scale(1.1);
    transition: .5s ease-out;
    box-shadow: 0 0 5px #ffffff,
              0 0 20px #ffffff,
              0 0 50px #ffffff,
              0 0 100px #ffffff;
    border-radius: 1rem;
}

.card-body:hover {
 box-shadow: 0px 0px 30px 1px rgba(255, 255, 255, 0.3);
}

</style>