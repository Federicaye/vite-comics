<template>
  <div>
    
    <AppNav/>
    <AppMain/>
    <AppNavShop/>
    <AppFooter/>
  </div>
</template>

<script>
import AppNav from './components/AppNav.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppNavShop from './components/AppNavShop.vue';
export default {
  name: 'App',
  components: {
    AppNav,
    AppMain,
    AppFooter,
    AppNavShop
  }
}
</script>

<style lang="scss" scoped></style>
