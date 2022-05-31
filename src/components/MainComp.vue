<template>
  <main>
      <RandomBlogItems/>
      <div class="container d-flex mt-4">
          <PostsComp
          :posts="popularPosts"/>
          <PostsComp/>
          <FeaturedPosts/>
      </div>
      <TagBandComp/>
      <ShowPostsComp/>
  </main>
</template>

<script>
import RandomBlogItems from "./RandomBlogItems.vue";
import PostsComp from "./PostsComp.vue";
import FeaturedPosts from "./FeaturedPosts.vue";
import TagBandComp from "./TagBandComp.vue";
import ShowPostsComp from "./ShowPostsComp.vue";

import Posts from "../assets/data/Posts";

export default {
name:'MainComp',
components:{
    RandomBlogItems,
    PostsComp,
    FeaturedPosts,
    TagBandComp,
    ShowPostsComp
},
data(){
    return{
        posts:Posts,
        popularPosts:[],
        recentPosts:[],
    }
},
methods:{
    popularPosts(){
        this.posts.forEach(post => {
            if(post.category==='popular'){
                this.popularPosts.push(post)
            }else{
              this.recentPosts.push(post)  
            }
        });
    }
}
}
</script>

<style lang="scss" scoped>
</style>