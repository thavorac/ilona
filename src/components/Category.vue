<template>
  <div :style="{ backgroundColor: color }">
      <!-- <img :src="'./assets/food-icons/' + {picture} + '.png'" alt=""> -->
      <img :src=picture alt="">
      <h1> {{ text1 }} </h1>
      <h2> {{ text2 }}</h2>

  </div>
</template>

<script>

  export default {
    name: "Category",
    props: ["color", "text1", "text2","picture"],
  };
  
</script>

  
<style scoped>
  
  div {
    width: 136px;
    height: 177px;
    flex-shrink: 0;
    border-radius: 10px;
    border: 1px solid var(--NestMart-Brand-1-Light, #81B13D);
    background: #F2FCE4;

    /* Shadow-1 */
    box-shadow: 20px 20px 40px 0px rgba(24, 24, 24, 0.07);
  }

  h1 {
    color: var(--NestMart-TextHeading, #253D4E);
    text-align: center;

    /* NestMart/Heading 6 */
    font-family: Quicksand;
    font-size: 16px;
    font-style: normal;
    font-weight: 700;
    line-height: 20px; /* 125% */
    letter-spacing: -0.006px;
  }
  
  h2 {
    color: var(--NestMart-Text-Muted, #B6B6B6);
    text-align: center;

    /* NestMart/ Text xs */
    font-family: Lato;
    font-size: 12px;
    font-style: normal;
    font-weight: 400;
    line-height: 18px; /* 150% */
  }

 img {
  width: 120px;
  height: 120px;
  display: flex;
  justify-content: center;
  align-items: center;
 }

  @font-face {
  font-family: "Quicksand";
  src: url('./public/fonts/Quicksand_Bold.otf');
}

  @font-face {
  font-family: "Lato";
  src: url('./public/fonts/Lato-Medium.ttf');
}
</style>