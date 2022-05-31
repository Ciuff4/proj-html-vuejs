<template>
  <section>
      <div class="container d-flex justify-content-around align-items-center h-100">
          <i @click="prevTag()"
          class="fa-solid fa-chevron-left"></i>
          <div
          v-for="(tag , index) in tags" :key="`tag(${index})`"
          :class="{'active' : counterTag===index}"
          class="tag">{{tag}}</div>
          <i @click="nextTag()"
          class="fa-solid fa-chevron-right"></i>
      </div>
      
  </section>
</template>

<script>
export default {
name:'TagBandComp',
data(){
    return{
        tags:[
            'gadgets',
            'photography',
            'lifestyle',
            'fashon',
            'recipes',
            'travel',
        ],
        counterTag:0,
    }
},
methods:{
    nextTag(){
        this.counterTag++;
        if (this.counterTag>this.tags.length-1) {
            this.counterTag=0;
        }
    },
    prevTag(){
        this.counterTag--;
        if (this.counterTag<0) {
            this.counterTag=this.tags.length-1;
        }
        return this.counterTag;
    }
}
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars.scss';
section{
    height: 80px;
    background-color:$primary-color;
    .tag{
        text-transform: uppercase;
        color: white;
        background-color: #212529;
        padding: 6px 12px;
        &.active{
           background-color: #32383E;
        }   
    }
}
</style>