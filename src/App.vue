<template>

  <div class="wrap">
    <div style="display: flex;">

      <div v-for="catego in categories" class="_fruit">
        <Category :color=catego.couleur :picture=catego.image :text1=catego.name :text2=catego.nbItems></Category>
      </div>
    </div>
    <div style="display: flex;">

      <div v-for="promo in promotion">
        <Promotion :text="promo.name" :img="promo.image" :color="promo.bg" :CButton="promo.ColorButton" :TButton="promo.TxtButton"></Promotion>
      </div>
    </div>
  </div>

</template>


<script>
import Onion from "./assets/food-icons/oignons.png";
import Vegetable from "./assets/food-icons/vegetables.png";
import Yogurt from "./assets/food-icons/yogurt.png";

import Burger from "./assets/food-icons/burger.png";
import Apple from "./assets/food-icons/apple.png";
import Kaki from "./assets/food-icons/kaki.png";
import Kiwi from "./assets/food-icons/kiwi.png";
import Cereal from "./assets/food-icons/cereal.png";
import Blueberry from "./assets/food-icons/blueberry.png";
import Letuce from "./assets/food-icons/letuce.png";
import Headphone from "./assets/food-icons/headphone.png";
import Chips from "./assets/food-icons/chips.png";
import Orange from "./assets/food-icons/orange.png";

import MyButton from "./components/MyButton.vue";
import Promotion from "./components/Promotion.vue";
import Category from "./components/Category.vue";


export default {
  name: "App",
  components: {
    MyButton,
    Promotion,
    Category,
  },
  data() {
    return {
      categories : [
        {
          name : "Cake and Milk",
          nbItems : "14 items",
          couleur : "#F2FCE4",
          image : new URL(Burger,import.meta.url).href,
        },
        {
          name : "Peach",
          nbItems : "17 items",
          couleur : "#FFFCEB",
          image : new URL(Kaki,import.meta.url).href,
        },
        {
          name : "Organic Kiwi",
          nbItems : "21 items",
          couleur : "#ECFFEC",
          image : new URL(Kiwi,import.meta.url).href,
        },
        {
          name : "Red Apple",
          nbItems : "68 items",
          couleur : "#F2FCE4",
          image : new URL(Apple,import.meta.url).href,
        },
        {
          name : "Snack",
          nbItems : "34 items",
          couleur : "#FFF3EB",
          image : new URL(Cereal,import.meta.url).href,
        },
        {
          name : "Black Plum",
          nbItems : "25 items",
          couleur : "#FFF3FF",
          image : new URL(Blueberry,import.meta.url).href,
        },
        {
          name : "Vegetables",
          nbItems : "65 items",
          couleur : "#F2FCE4",
          image : new URL(Letuce,import.meta.url).href,
        },
        {
          name : "Headphone",
          nbItems : "33 items",
          couleur : "#FFFCEB",
          image : new URL(Headphone,import.meta.url).href,
        },
        {
          name : "Cake and Milk",
          nbItems : "26 items",
          couleur : "#F2FCE4",
          image : new URL(Chips,import.meta.url).href,
        },
        {
          name : "Orange",
          nbItems : "63 items",
          couleur : "#FFF3FF",
          image : new URL(Orange,import.meta.url).href,
        },
      ],
      promotion : [
        {
          name : "Everyday Fresh & Clean with Our Products",
          bg : "#F0E8D5",
          image : new URL(Onion,import.meta.url).href,
          TxtButton : "Shop Now",
          ColorButton : "#3BB77E",
        },
        {
          name : "Make your Breakfast Healthy and Easy",
          bg : "#F3E8E8",
          image : new URL(Yogurt,import.meta.url).href,
          TxtButton : "Shop Now",
          ColorButton : "#3BB77E",
        },
        {
          name : "The best Organic Products Online",
          bg : "#E7EAF3",
          image : new URL(Vegetable,import.meta.url).href,
          TxtButton : "Shop Now",
          ColorButton : "#FDC040",
        },
      ],
    }
  },
};
</script>


<style scoped>
._fruit {
  display: flex;
  margin-right: 25px;
}

.wrap {
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

</style>