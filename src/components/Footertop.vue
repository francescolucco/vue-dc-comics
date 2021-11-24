<template>
  <div class="footer-top">
    <div class="container">
      <div class="menu-footer">
        <div 
          v-for="(item, index) in listMenuFooter"
          :key="`menu-footer-${index}`" 
          class="col">
          <div class="title">{{item.title}}</div>
          <div 
            v-for="(voice, index) in item.voices"
            :key="`voice-menu-${index}`" 
            class="voice-menu">{{voice}}</div>
        </div>
      </div>
      <div class="img-logo-footer">
        <img src="../assets/img/dc-logo-bg.png" alt="">
      </div>
    </div>
  </div>
</template>

<script>
export default {
   name: 'Footertop',
   data(){
     return{
      listMenuFooter: [
        {
          title: 'dc comics',
          voices: [
            'charachters',
            'Comics',
            'Movies',
            'TV',
            'Games',
            'Videos',
            'News'
          ]
        },
        {
          title: 'dc',
          voices: [
            'Terms Of Use',
            'Privacy policy (New)',
            'Ad Choices',
            'Jobs',
            'Subscription',
            'Talent Workshops',
            'CPSC Certificates',
            'Ratings',
            'Shop Help',
            'Contact US'
          ]
        },
        {
          title: 'sites',
          voices: [
            'DC',
            'MAD Magazine',
            'DC Kids',
            'DC Universe',
            'DC Power Visa'
          ]
        },
        {
          title: 'shop',
          voices: [
            'Shop DC',
            'Shop DC Collectibles'
          ]
        }
      ]
     }
   }
}
</script>

<style lang="scss">
  
@import "../assets/style/vars.scss";
@import "../assets/style/mixin.scss";

.footer-top{
  height: 480px;
  background-image: url('../assets/img/footer-bg.jpg');
  overflow: hidden;
  .container{
    height: 100%;
    @include between();
    .menu-footer{
      height: 480px;
      padding: 50px 0;
      .col{
        float: left;
        width: 150px;
        padding-bottom: 40px;
        .title{
          color: white;
          font-size: 1.1rem;
          font-weight: bold;
          text-transform: uppercase;
          margin-bottom: 20px;
        }
        .voice-menu{
          color: lightgrey;
          font-size: 0.8rem;
          padding-bottom: 10px;
          cursor: pointer;
          &:hover{
            color: white;
          }
        }
      }
      }
    .img-logo-footer{
      height: 100%;
      @include center();
      img{
        width: 155%;
        flex-shrink: 0;
        flex-basis: 0;
      }
    }
  }
}

</style>