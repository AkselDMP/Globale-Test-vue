<template>
  <div>
    <section class="w-screen h-screen bg-white">
      <div id="product" class="pt-middle flex items-center justify-center">
        <div id="product-image">
          <img :src="image"/>
        </div>
        <div id="info-product">
          <p>{{product}}</p>
          <p v-if="inSock">Test123</p>
          <p v-else>Test456</p>
          <button v-on:click="AddMore">Add product</button>
          <p>Total ({{cart}})</p>
  
        <div v-for:="varia in varias">
            <p @mouseover="updateProduct(varia.variaImg)">{{varia.variaColor}}</p>
        </div>
        </div>
      </div>
    </section>  
  </div>
</template>
      

  
  
  <script>
  
  export default {
    data: function () {
      return {
        product:'Socks',
        inSock: false,
        cart: 0,
  
      AddMore: function(){
        this.cart += 1
      },
  
      varias: [
        {
          variaColor: "green",
          variaImg: "./components/green.svg"
        },
        {
          variaColor: "grey",
          variaImg: "./components/grey.svg"
        }
      ],
  
      updateProduct (variaImg){
        this.image = variaImg
      },
  
        image: "./components/green.svg",
      };
    },
  };
  </script>
  
  <style>
  @import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800;900&display=swap");
  html,
  body {
    font-family: "Poppins", sans-serif;
  }
  </style>
  




