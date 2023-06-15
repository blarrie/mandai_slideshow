<template style="margin: auto;">
  <Carousel :autoplay="5000" :wrap-around="true" class="carousel">

    <template #slides>
      <Slide v-for="photo in photos" :key="photo">
        <div class="carousel__item">
          <img :src="`src/assets/${photo}`" style="height: 100vh;">

        </div>
      </Slide>
    </template>



  </Carousel>
</template>

<script>
import { defineComponent } from "vue";
import { Carousel, Slide } from "vue3-carousel";
import "vue3-carousel/dist/carousel.css";

export default defineComponent({
  name: "Autoplay",
  components: {
    Carousel,
    Slide,
  },
  data() {
    return {
      photos: [
        "p1.jpg",
        "p2.jpg",
        "p3.jpg",
        "p4.jpg",
        "p5.jpg",
        "p6.jpg",
        "p7.jpg",
      ],
    };
  },
});
</script>

<style>
  .carousel__item {
    margin: 0;
    padding: 0;
    height: 100vh;
    width: 100%;
    background-color: var(--vc-clr-primary);
    color: var(--vc-clr-white);
    display: flex;
    justify-content: center;
    align-items: center;
    margin: auto;
  }

  .carousel__slide {
    background-color: black;
    margin: 0;
    padding: 0;
    overflow: hidden;
  }
  
</style>