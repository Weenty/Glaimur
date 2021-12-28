<template>
  <div>
    <VueSlickCarousel v-bind="settings">
      <div class="card-category"> <img src="img/pXs0NUsq678.jpg" alt=""> Диваны</div>
    </VueSlickCarousel>
  </div>
</template>

<script>
import VueSlickCarousel from "vue-slick-carousel";
import "vue-slick-carousel/dist/vue-slick-carousel.css";
import "vue-slick-carousel/dist/vue-slick-carousel-theme.css";
export default {
  components: { VueSlickCarousel },
  data() {
    return {
      settings: {
        infinite: true,
        slidesToShow: 5,
        speed: 500,
        rows: 1,
        slidesPerRow: 1,
      },
    };
  },
};
</script>

<style scoped>
.card-category {
    display: flex;
}
</style>