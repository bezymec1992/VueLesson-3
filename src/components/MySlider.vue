<template>
   <div id="carousel" class="carousel slide" data-bs-ride="carousel">
      <div class="carousel-inner">
        <div v-for="(slide, index) in slides" :key="index" :class="['carousel-item', { 'active': currentIndex === index }]">
          <img :src="slide.src" class="d-block w-100" :alt="slide.alt">
        </div>
      </div>
      <button class="carousel-control-prev" @click="prevSlide" type="button">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
      </button>
      <button class="carousel-control-next" @click="nextSlide" type="button">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
      </button>
    </div>
</template>

<script>

export default {
  name: 'MySlider',
  
  props: {
    slides: {
      type: Array,
      required: true
    }
  },
  data() {
      return {
        currentIndex: 0,
      };
    },
    methods: {
        prevSlide() {
          this.currentIndex = (this.currentIndex - 1 + this.slides.length) % this.slides.length;
        },
        nextSlide() {
          this.currentIndex = (this.currentIndex + 1) % this.slides.length;
        }
      }
}

</script>

<style scoped>
 .carousel-inner {
  max-width: 400px;
  width: 100%;
  margin: 0 auto;
 }
 button {
  background-color: black;
  width: 50px;
  height: 50px;
  top: 50%;
  transform: translateY(-50%);
 }
</style>