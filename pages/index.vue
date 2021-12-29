<template>
  <div>
    <div class="background-frame"></div>
    <div class="container">
      <Navbar />
    </div>
    <div class="carousel"><Carousel /></div>
    <div class="CategoryList"> <CategoryList /> </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.CategoryList {
  margin: auto;
  max-width: 96%;
  height: 780px;
  padding-top: 58px; 
}
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
@media (max-width: 1040px) {
  .carousel {
    display: none;
  }
  .background-frame {
    display: none;
  }
}
</style>
