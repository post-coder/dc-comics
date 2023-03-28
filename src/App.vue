<script>
import AppBuy from './components/AppBuy.vue';
import AppComics from './components/AppComics.vue';
import AppFooter from './components/AppFooter.vue';
import AppNav from './components/AppNav.vue';

export default {
  data() {
    return {
      
    }
  },

  components: {
    AppBuy,
    AppFooter,
    AppComics,
    AppNav
}
}
</script>

<template>

  <AppNav></AppNav>

  <!-- CHARACTER CONTAINER  -->
  <AppComics></AppComics>

  
  <AppBuy>
    
  </AppBuy>


  <AppFooter>

  </AppFooter>

</template>

<style lang="scss" scoped>


</style>
