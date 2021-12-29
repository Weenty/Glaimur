<template>
  <b-container class="bv-example-row" style="max-width:1300px  ">
    <div class="title_sale">Товары</div>
    <b-row>
      <b-col class="card_hover" cols="12" sm="12" md="6" lg="4" xl="3" v-for="main in cards" :key="main.id" >
          <button class="card_button">
          <div class="main_card" >
          <div class="img_block">
            <img class="img_card" :src="'img/' + main.src" alt="error" />
          </div>
          <div class="hover_bg">
          <div class="main_title">{{main.title}}</div>
          <div class="main_subtitle">{{main.subtitle}}</div>
          <div class="price_views">
 <div class="main_price">{{main.price}} Руб</div>
  <div class="main_price2">
    <img class="img_c" :src="'img/' + main.imgviw" alt="error" />
    <div class="viv">
{{main.views}}
    </div>
  </div>
          </div>
             
          </div>
        </div>
          </button>
     
      </b-col>
    </b-row>
    <div class="button_hower">
      <button class="showmore">
      Показать больше
    </button>
    </div>
    
  </b-container>
</template>

<script>

export default {
  data() {
    return {
      cards: [{
    id: 0,
    title: "Чайный стол",
    subtitle: "Мебель для дома",
    price: 23999,
    src: "image1.png",
    views:"2000",
    imgviw:"image 15.png"
  },
  {
    id: 1,
    title: "Жесткий диван",
    subtitle: "Диваны",
    price: 42999,
    src: "image 3.png",
    views:"3500",
    imgviw:"image 15.png"
  },
  {
   id: 2,
    title: "Винтелятор",
    subtitle: "Для дома",
    price: 11999,
    src: "image 4.png",
    views:"5000",
    imgviw:"image 15.png"
  },
  {
    id: 3,
    title: "Ваза",
    subtitle: "Для кухни",
    price: 4999,
    src: "image 8.png",
    views:"2300",
    imgviw:"image 15.png"
  },
  {
    id: 4,
    title: "Лампа",
    subtitle: "Для спальни",
    price: 2999,
    src: "image 9.png",
    views:"1000",
    imgviw:"image 15.png"
  },
  {
    id: 0,
    title: "Кружка Элитная",
    subtitle: "Мебель для дома",
    price: 799,
    src: "image 6.png",
    views:"1300",
    imgviw:"image 15.png"
  },
  {
    id: 0,
    title: "Мягкая кровать",
    subtitle: "Мебель для дома",
    price: 65999,
    src: "image 7.png",
    views:"5400",
    imgviw:"image 15.png"
  },
  {
   id: 0,
    title: "Чайный стол",
    subtitle: "Мебель для дома",
    price: 23999,
    src: "image1.png",
    views:"2000",
    imgviw:"image 15.png"
  }]
    };
  },

};
</script>

<style>
.hover_bg{
  background: #F4F5F7;
}
.img_c{
  width: 31px;
height: 15px;
}
.main_price2{
  display: flex;
  align-items: center;
}
.button_hower{
  display: flex;
   justify-content: center;
   padding-bottom: 50px ;
}
.showmore{
  
  width: 245px;
height: 48px;
    background: #FFFFFF;
    color:#E89F71;
/* Color / Primary */

border: 1px solid #E89F71;
box-sizing: border-box;
}
.main_title{
  font-family: Actor;
font-style: normal;
font-weight: normal;
font-size: 24px;
line-height: 120%;
/* identical to box height, or 29px */


/* Color / Gray 1 */

color: #3A3A3A;
}
.main_subtitle{
font-family: Actor;
font-style: normal;
font-weight: normal;
font-size: 16px;
line-height: 150%;
/* identical to box height, or 24px */


/* Color / Gray 3 */

color: #898989;
}
.add_button{
  max-width: 300px;
  max-height: 50px;
}
.title_sale{
    text-align: center;
    padding-bottom: 20px;
}
.card_button{
     outline: none; /* Для синий ободки */
  border: 0;
  background: transparent;
}
.price_views{
display: flex;
justify-content: space-evenly;
}
.main_card {

}
.card_hover{
  padding-bottom: 40px;
}
.img_block {
  position: relative;
}
.img_discount{
  position: absolute;
  background-color: violet;
  top: 0px;
  right: 0px;
}
.img_card {
  max-width: 300px;
  max-height: 380px;
  width: 250px;
  height: 300px;
}
.title_sale {
  font-size: 40px;
  text-transform: uppercase;
}
.main_price {
  padding-bottom: 0px;
}
</style>