<template>
  <div>
    <div class="row">
      <div class="col-xl-10 col-lg-10 col-md-9 col-sm-8 col-5"></div>
      <div class="col" id="carousel-button-next">
        <img height="48px" src="img/aat2WX8QlnU.jpg" alt="" /><img
          style="padding-left: 10px"
          height="48px"
          src="img/CRujE7cdOV8.jpg"
          alt=""
        />
      </div>
    </div>
    <VueSlickCarousel v-bind="settings">
      <div style="width: 934px">
        <img
          width="934px"
          height="623px"
          src="img/MDYe0dPvoqE.jpg"
          draggable="false"
          alt=""
        />
      </div>
      <div style="width: 934px">
        <img
          width="934px"
          height="623px"
          src="img/X-VeDkUCRvk.jpg"
          draggable="false"
          alt=""
        />
      </div>
      <div style="width: 934px">
        <img
          width="934px"
          height="623px"
          src="img/XygegQuVhT0.jpg"
          draggable="false"
          alt=""
        />
      </div>
    </VueSlickCarousel>
    <div class="top-frame">
      <div class="frame-container">
        <div class="top-frame-hight-text">Высококачес<wbr>твенно и<br> просто</div>
        <div class="top-frame-low-text">
          Наша мебель изготовлена из отборных материалов самого высокого
          качества, которые подходят для дома вашей мечты
        </div>
        <button class="top-frame-button">
          <div class="top-frame-button-text">Купить сейчас</div>
        </button>
      </div>
    </div>
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
        centerMode: true,
        variableWidth: true,
        speed: 300,
        centerPadding: "32px",
      },
    };
  },
};
</script>

<style scoped>
#carousel-button-next {
  margin-bottom: 22px;
}
.top-frame {
  top: 68px;
  left: 100px;
  background-color: white;
  opacity: 0.9;
  z-index: 999;
  position: absolute;
  width: 494px;
  height: 553px;
}
.top-frame-hight-text {
  font-family: Actor;
  font-style: normal;
  font-weight: normal;
  font-size: 56px;
  line-height: 120%;
  color: #3a3a3a;
  word-break: break-all;
}
.top-frame-low-text {
  margin-top: 16px;
  font-family: Actor;
  font-style: normal;
  font-weight: normal;
  font-size: 20px;
  line-height: 150%;
  color: #898989;
}
.top-frame-button-text {
  font-family: Actor;
  font-style: normal;
  font-weight: normal;
  font-size: 20px;
  line-height: 150%;
  color: #ffffff;
}
.top-frame-button {
  margin-top: 18px;
  border: 0;
  width: 374px;
  height: 78px;
  background: #e89f71;
}
.frame-container {
  padding-top: 60px;
  width: 374px;
  margin: auto;
}
</style>