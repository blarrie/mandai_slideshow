<template style="margin: auto;">
  <Carousel :autoplay="5000" :wrap-around="true" class="carousel">

    <template #slides>
      <Slide v-for="photo in photos" :key="photo">
        <div class="carousel__item">
          <img :src="`src/assets/${photo}`" style="height: 100vh;">

        </div>
        <!-- <img src="https://cdn.britannica.com/39/7139-050-A88818BB/Himalayan-chocolate-point.jpg?w=400&h=300&c=crop" alt=""> -->
      </Slide>
    </template>


    <template #addons>
      <Pagination />
    </template>
  </Carousel>
</template>

<script>
import { defineComponent } from "vue";
import { Carousel, Pagination, Slide } from "vue3-carousel";
import "vue3-carousel/dist/carousel.css";

export default defineComponent({
  name: "Autoplay",
  components: {
    Carousel,
    Slide,
    Pagination,
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
    height: 100%;
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
    padding: 50%;
    overflow: hidden;
  }
  
</style>