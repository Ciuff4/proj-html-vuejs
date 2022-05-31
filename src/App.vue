<template>
  <div id="app">
    <HeaderComp/>
    <MainComp/>
    <FooterComp/>
  </div>
</template>

<script>
import MainComp from './components/MainComp.vue';
import HeaderComp from './components/HeaderComp.vue';
import FooterComp from './components/FooterComp.vue';


export default {
    name: "App",
    components: { MainComp, HeaderComp, FooterComp }
}
</script>

<style lang="scss">
@import './assets/style/general.scss';
@import './assets/style/vars.scss'
</style>
