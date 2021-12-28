<template>
  <div>
    <div class="background-frame"></div>
    <div class="container">
      <Navbar />
    </div>
    <div class="carousel"><Carousel /></div>
    <CategoryList />
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.carousel {
  margin: auto;
  max-width: 96%;
  padding-top: 58px;
}
.background-frame {
  position: absolute;
  width: 964px;
  height: 774px;
  left: 0px;
  top: 0px;
  background: #f9f1e7;
}
@media (max-width: 965px) {
  .carousel {
    display: none;
  }
  .background-frame {
    display: none;
  }
}
</style>
