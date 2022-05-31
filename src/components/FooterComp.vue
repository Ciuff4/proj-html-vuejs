<template>
  <footer>
      <TopFooterComp/>
      <BottomFooterComp/>
  </footer>
</template>

<script>
import TopFooterComp from "./TopFooterComp.vue";
import BottomFooterComp from "./BottomFooterComp.vue";

export default {
name:'FooterComp',
components:{TopFooterComp,BottomFooterComp}
}
</script>

<style lang="scss" scoped>

</style>