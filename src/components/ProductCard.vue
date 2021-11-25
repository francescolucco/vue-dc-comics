<template>
  <div class="card">
     <div class="box-img">
         <img :src="card.thumb">
     </div>
     <div class="title">{{card.series}}</div>
     <span class="price">{{card.price}}</span>
  </div>
</template>

<script>
export default {
   name: 'ProductCard',
   props:{
      card: Object,
   }
}
</script>

<style lang="scss">

@import '../assets/style/mixin.scss';
 @import "../assets/style/vars.scss";
 
 .card{
   @include column();
   color: white;
   text-align: start;
   padding: 15px;
   cursor: pointer;
   width: calc(100% / 6);
   &:hover .title, &:hover .price{
      transition: 0.25s;
      font-weight: bold;
      color:  $merchandaise-color;
   }
   &:hover .box-img{
      transition: 0.25s;
      border: 4px solid  $merchandaise-color;
   }
      .box-img{
         width: calc(100vh / 4.75);
         height: calc(100vh / 4.75);
         overflow: hidden;
         margin-bottom: 30px;
         img{
            width: 100%;
          }
   }
   .title{
      font-size: 17px;
      text-transform: uppercase;
      margin-bottom: 10px;
   }
   .price{
      color: lightgray;
      font-size: 13px;
   }

}
</style>