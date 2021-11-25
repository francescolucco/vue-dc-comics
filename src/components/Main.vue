<template>
<main>
  <JumbotronHome />
  <div class="container">
    <button class="current-series">Current series</button>
    <div class="box-card">
      <ProductCard 
        v-for="(item, index) in Cards"
        :key="index"
        :card="item"
        />
    </div>
    <button class="load-more">load more</button>
  </div>
</main>
</template>

<script>

import Cards from '../assets/data/dc-comics'
import JumbotronHome from './JumbotronHome.vue'
import ProductCard from './ProductCard.vue'

export default {
   name: 'Main',
   components:{
     JumbotronHome,
     ProductCard,
   },
   data(){
     return{
       Cards,
     }
   }
}
</script>

<style lang="scss">
 @import "../assets/style/vars.scss";
 @import "../assets/style/mixin.scss";

main{
  background-color: black;
  width: 100%;
  .container{
    position: relative;
    text-align: center;
    button{
      text-transform: uppercase;
      color: white;
      background-color: $merchandaise-color;
      cursor: pointer;
      border: none;
      font-weight: bold;
    }
    .current-series{
      position: absolute;
      top: 0;
      left: 0;
      transform: translateY(-50%);
      font-size: 23px;
      padding: 10px 27px;
      &:hover{
        color: black;
        background-color: white;
        transition: 0.3s;
        }
    }
    .box-card{
      @include wrap();
      padding: 65px 0 40px 0;
      width: 100%;
    }
    .load-more{
      font-size: 12px;
      padding: 8px 47px;
      margin-bottom: 30px;
      text-align: center;
      border: 2px solid black;
      &:hover{
          border: 2px solid white;
          color: white;
          background-color: rgba(255, 255, 255, 0.445);
          transition: 0.3s;
        }
    }
  }
}

</style>