<template>
    <button :style="{ backgroundColor: color }">
      {{ text }}
      <font-awesome-icon icon="phone" class="font" />
      <!-- <i class="fas fa-arrow-right"></i> -->
    </button>
  </template>
  
  <script>

  export default {
    name: "MyButton",
    props: ["text", "color"],
  };


  </script>
  

  <style scoped>

  .font {
    margin-left: 10px;
  }

  button {
    position: relative;
    border: none;
    padding: 8px 15px;
    justify-content: center;
    align-items: center;
    gap: 10px;
    color: white;
    border-radius: 3px;
    box-shadow: 14px 14px 36px 0px rgba(85, 85, 85, 0.10);
  }

  
  </style>