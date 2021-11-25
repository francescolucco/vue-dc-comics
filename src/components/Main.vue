<template>
<main>
  <JumbotronHome />
  <div class="container">
    <h3>-->Content goes here </h3>
  <ProductCard />
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
main{
  background-color: black;
  h3{
    color: white;
    padding-top: 30px;
  }
}

</style>