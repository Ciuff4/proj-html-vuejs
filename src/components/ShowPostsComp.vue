<template>
  <section>
      <div class="container d-flex pt-5">
          <div class="side">
              <BigPostBolgComp
              v-for=" (post , index) in posts" :key="`bigPost(${index})`"
              :post="post"/>
          </div>
          <div class="aside ps-3">
              <h6>LATEST FROM TWITTER</h6>
              <div class="mb-1">
                  <p class="mb-0"><i class="fa-brands fa-twitter"></i>If you have any suggestions for the next updates, let us know</p>
                  <span>01:05 PM Sept 18th</span>
              </div>
              <div class="mb-1">
                  <p class="mb-0"><i class="fa-brands fa-twitter"></i>We have just updated Porto Admin. Check the changelog for more information.</p>
                  <span>01:04 PM Sept 18th</span>
              </div>
              <div class="instagram-photos mt-5">
                <h6>PHOTOS FROM INSTAGRAM</h6>
                <div class="d-flex flex-wrap">
                  <div class="box">
                      <img src="../assets/images/29415304_166583630713703_1032667922171953152_n.jpg" alt="">
                  </div>
                  <div class="box">
                      <img src="../assets/images/29415620_196477127626244_3250318472361541632_n.jpg" alt="">
                  </div>
                  <div class="box">
                      <img src="../assets/images/29739607_2020680068220520_4509928046932787200_n.jpg" alt="">
                  </div>
                  <div class="box">
                      <img src="../assets/images/30077195_2066750973610181_3733150062893596672_n.jpg" alt="">
                  </div>
                  <div class="box">
                      <img src="../assets/images/30078414_1274410412703843_8290935809419247616_n.jpg" alt="">
                  </div>
                  <div class="box">
                      <img src="../assets/images/30087804_253872848488989_8792603541668626432_n.jpg" alt="">
                  </div>
                </div>
              </div>
              <div class="mb-5">
                  <h6 class="mt-3">TAGS</h6>
                  <div class="tags">
                      <span>DESIGN</span>
                      <span>BRANDS</span>
                      <span>VIDEO</span>
                      <span>BUSINESS</span>
                      <span>TRAVEL</span>
                  </div>
              </div>
              <div>
                  <h6>FIND US ON FACEBOOK</h6>
                  <div class="facebook-name d-flex align-items-center">
                      <span>Okler themes</span> 
                  </div>
              </div>
          </div>
          
      </div>
  </section>
</template>

<script>
import BigPostBolgComp from "./BigPostBolgComp.vue";

import Posts from "../assets/data/Posts";

export default {
name:'ShowPostsComp',
components:{BigPostBolgComp},
data(){
   return{
       posts:Posts
   }
}
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars.scss';
.side{
    width: 70%;
}
.aside{
    width: 30%;
    h6{
        font-weight: bold;
    }
    p{
        color: #B7B7B7;
        i{
            color: #212529;
        }
    }
    span{
        font-size: 0.8rem;
        color:$primary-color ;
    }
    .instagram-photos{
        width: 100%;
        .box{
        width: calc(100% /3 );
        height: calc(100% /3);
        img{
            width: 100%;
        }
        }
    }
    .tags span{
        color: white;
        background-color: #212529;
        border-radius: 10px;
        font-weight: bold;
        margin: 0 3px;
        padding: 3px 5px;
    }
    .facebook-name{
        height: 50px;
        color: $primary-color;
        border-left: 3px solid #EEEEEE;
        span{
            padding-left: 10px;
            cursor: pointer;
        }
    }
    
}
</style>