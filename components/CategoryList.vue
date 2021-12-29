<template>
  <div>
    <div class="category-item-with-image">
      <VueSlickCarousel v-bind="settings">
        <button
          v-for="(item, index) in category"
          :key="index"
          class="card-category"
          @click="dropdown=item.name"
        >
          <div class="row">
            <div class="col-xl-2 col-lg-5 col-6">
              <img class="card-img" :src="'img/' + item.img" alt="" />
            </div>
            <div class="col">
              <div class="card-category-text">{{ item.name }}</div>
            </div>
          </div>
        </button>
      </VueSlickCarousel>
    </div>
    <div class="category-item-no-image">
      <b-dropdown
        :text="dropdown"
        block
        variant="light"
        class="m-2"
        menu-class="w-100"
      >
        <b-dropdown-item
          @click="dropdown = item.name"
          v-for="(item, index) in category"
          :key="index"
          style="text-align: center"
          >{{ item.name }}</b-dropdown-item
        >
      </b-dropdown>
    </div>
    <b-container style="padding-top:40px" class="vh-100 text-center" align-v="center">
  <b-row>
    <b-col></b-col>
    <b-col><b-button @click="dropdown='All'" class="clear-button" variant="light">Очистить</b-button></b-col>
    <b-col></b-col>
  </b-row>
</b-container>
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
      dropdown: "All",
      settings: {
        infinite: true,
        slidesToShow: 5,
        speed: 500,
        rows: 1,
        slidesPerRow: 1,
      },
      category: [
        {
          img: "pXs0NUsq678.jpg",
          name: "Диваны",
        },
        {
          img: "pXs0NUsq678.jpg",
          name: "Товары для дома",
        },
        {
          img: "pXs0NUsq678.jpg",
          name: "Для кухни",
        },
        {
          img: "pXs0NUsq678.jpg",
          name: "для спальни",
        },
        {
          img: "pXs0NUsq678.jpg",
          name: "Для прихожей",
        },
        {
          img: "pXs0NUsq678.jpg",
          name: "Для вас",
        },
      ],
      itemSize: true,
    };
  },
};
</script>

<style scoped>
.card-category {
  display: flex;
  outline: none;
  border: 0;
  background: transparent;
}
.card-img {
  width: 78px;
  height: 67px;
}
.card-category-text {
  padding-top: 29px;
}
.category-item-no-image {
  display: none;
}
.clear-button {
  width: 150px;
  height: 45px;
}
@media (max-width: 1040px) {
  .category-item-with-image {
    display: none;
  }
  .category-item-no-image {
    display: block;
  }
}
</style>