<template>
  <div>
    <Header />
    <Main />
    <Merchandise />
    <Footertop />
    <Footerbottom />

  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Merchandise from './components/Merchandise.vue'
import Footertop from './components/Footertop.vue'
import Footerbottom from './components/Footerbottom.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Merchandise,
    Footertop,
    Footerbottom
  }
}
</script>

<style lang="scss">
  @import "./assets/style/vars.scss";
  @import "./assets/style/generals.scss";
  @import "./assets/style/utilities.scss";
  @import "./assets/style/mixin.scss";

</style>
