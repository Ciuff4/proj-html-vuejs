<template>
  <section>
      <h6> POPULAR POSTS</h6>
      <ul class="pl-0 flex-column">
          <li
          v-for="post in posts" :key="`post(${post.category})`"
          class="d-flex pb-3">
              <img :src="post.image" alt="">
              <div class="text ps-3">
                   <p class="m-0">{{post.title}}</p>
                   <span>{{post.date_published}}</span>
              </div>
          </li>
      </ul>
  </section>
</template>

<script>
export default {
name:'PostsComp',
props:{
    posts:Array
}
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars.scss';

section{
    width: calc(100% / 3);
    li{
        width: 100%;
        border-bottom: 1px solid #F7F7F7;
        padding-bottom: 10px;
    }
}
img{
    width: 50px;
    height: 50px;
}
p{
    text-transform: capitalize;
    &:hover{
        color: $primary-color;
    }
}
span{
    color: #B7B7B7;
    font-size: 0.8rem;
}
</style>