<template>
  <div class="_promo" :style="{ backgroundColor: color }">
    <div class="_render">
      <h1>{{ text }}</h1>
    </div>
    <div class="_img">
      <img :src=img alt="">
    </div>
    <MyButton :text="TButton" :color="CButton" class="_btn"></MyButton>
  </div>
</template>

<script>

import MyButton from './MyButton.vue';

export default {
  name: "Promotion",
  props: ["text","color","CButton","TButton","img"],
  components: {
    MyButton,
  }
};


</script>

<style scoped>

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

._promo {
    margin: 20px 20px 0 0;
    width: 512px;
    height: 300px;
    position: relative;
    border-radius: 10px;
}


._render {
    position: absolute;
    width: calc(512px-200px);
    position: relative;
}

h1 {
  position: absolute;
  top: 75px;
  left: 48px;
  width: 271px;
  color: var(--NestMart-TextHeading, #253D4E);
  font-family: Quicksand;
  font-size: 28px;
  font-style: normal;
  font-weight: 700;
  line-height: 32px;
  letter-spacing: -0.01px;
  z-index: 10;
}

._img {
    position: absolute;
    z-index: 0;
    display: flex;
    justify-content: end;
    align-items: end;
    width: 200px;
    height: 250px;
    right: 0px;
    bottom: 0px;
}

._btn{
    position: absolute;
    left: 48px;
    bottom: 75px
}

img {
  height: 249px;
}
</style>