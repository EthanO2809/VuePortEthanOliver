<template>
    <div>
        <div class="container">
            <div class="row mt-5 mb-5">
                <div class="col-4" v-for="item in testimonials" :key="item.id">
                    <div class="card mb-5" style="width: 18rem;">
                        <img :src="item.image" style="height: 24rem;" class="card-img-top" :alt="item.name">
                        <div class="card-body">
                          <p class="card-text">{{ item.name }}</p>
                          <p class="card-text">{{ item.role }}</p>
                          <p class="card-text">{{ item.words }}</p>
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
            testimonials() {
                return this.$store.state.testimonials
            }
        },
        mounted() {
            this.$store.dispatch('fetchTestimonials')
        }
    }
</script>

<style scoped>

</style>