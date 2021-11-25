<template>
  <header class="container">
    <div class="box-logo">
      <img src="../assets/img/dc-logo.png" alt="logo">
    </div>
    <nav class="menu-header">
      <ul>
        <li v-for="(link, index) in links" 
          :key="`menu-header-${index}`"
          @click="getActive(index)" 
          :class="{active: link.current}">
          <a :class="{active: link.current}" href="#">{{link.text}}</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
   name: 'Header',
   data(){
     return{
       links:[
         {
           url: '/characters',
           text: 'characters',
           current: false,
         },
         {
           url: '/',
           text: 'comics',
           current: true
         },
         {
           url: '/movies',
           text: 'movies',
           current: false
         },
         {
           url: '/tv',
           text: 'tv',
           current: false
         },
         {
           url: '/games',
           text: 'games',
           current: false
         },
         {
           url: '/collectibles',
           text: 'collectibles',
           current: false
         },
         {
           url: '/videos',
           text: 'videos',
           current: false
         },
         {
           url: '/fans',
           text: 'fans',
           current: false
         },
         {
           url: '/news',
           text: 'news',
           current: false
         },
         {
           url: '/shop',
           text: 'shop',
           current: false
         },
       ],
     }
   },
   methods:{
    getActive(index){

      this.links.forEach((item)=>{
        item.current = false;
      });
      this.links[index].current = true;
    },

  }
}
</script>

<style lang="scss">

@import "../assets/style/vars.scss";
@import "../assets/style/mixin.scss";

  header{
    height: 130px;
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .box-logo img{
      padding: 20px 20px 20px 0;
    }
    nav{
      height: 100%;
      ul{
        @include center();
        list-style: none;
        height: 100%;
        li{
          height: 100%;
          margin-left: 25px;
          @include center();
          border-bottom: 5px solid white;
          cursor: pointer;
          &:hover{
            border-bottom: 5px solid $logo-color;
            transition: 0.1s;
          }
          &:hover a{
            color: $logo-color;
            transition: 0.1s;
            font-size: bold;
          }
          &.active{
            border-bottom: 5px solid $logo-color;
          }
          a{
            text-decoration:none;
            color: $primary-color;
            text-transform: uppercase;
            font-weight: bold;
            &.active{
              color: $logo-color;
            }
          }
        }
      }
    }
    
  }

</style>