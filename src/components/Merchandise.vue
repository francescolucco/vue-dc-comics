<template>
  <section class="merchandise">
    <div class="container">
      <div 
        v-for="(item, index) in shops"
        :key="`section-merchandise-${index}`"
        class="action-shop">
        <img :src="require(`../assets/img/${item.url}`)" alt="">
        <h1>{{item.text}}</h1>
      </div>
    </div>
  </section>
</template>

<script>
export default {
   name: 'Merchandise',
   data(){
     return{
       shops:[
         {
           url: 'buy-comics-digital-comics.png',
           text: 'digital comics',
         },
         {
           url: 'buy-comics-merchandise.png',
           text: 'dc merchandise',
         },
         {
           url: 'buy-comics-subscriptions.png',
           text: 'subscription',
         },
         {
           url: 'buy-comics-shop-locator.png',
           text: 'comic shop locator',
         },
         {
           url: 'buy-dc-power-visa.svg',
           text: 'dc power visa',
         },
       ]
     }
   }
}
</script>

<style lang="scss">

@import "../assets/style/vars.scss";
@import "../assets/style/mixin.scss";

section.merchandise{
  height: 150px;
  background-color: $merchandaise-color;
  &:hover{
    transition: 0.5s;
    filter: invert(1);
  }
  .container{
    @include around();
    height: 100%;
  .action-shop{
      @include center();
      cursor: pointer;
      height: 100%;
      &:hover img, &:hover h1{
          filter: invert(1);
          transform: scale(1.075);
          transition: 0.25s;
        }
      img{
        height: 35%;
              }
      h1{
        color: white;
        text-transform: uppercase;
        margin-left: 7px;
        margin-right: 20px;
        font-size: 0.75rem;
      }
    }
  }
}

</style>