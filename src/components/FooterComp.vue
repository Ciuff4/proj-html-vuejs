<template>
  <footer>
      <div class="footer-top">
          <div class="container cg-container d-flex">
              <div class="etichetta">
                <span>Get in touch</span>
              </div>
          </div>
          <div class="container d-flex">
              <div class="row row-cols-4">
                  <div class="col">
                  <h6>ABOUT THE BLOG</h6>
                  <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ut doloribus debitis corporis aliquid itaque!</p>
                  <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Laudantium maiores minima sint autem ad repudiandae!...</p>
                  <h6>VIEW MORE<i class="fa-solid fa-chevron-right"></i></h6>
              </div>
              <div class="col">
                  <h6>RECENT POSTS</h6>
                  <div class="d-flex mb-3">
                      <img src="../assets/images/our-office-4-square.jpg" alt="">
                      <div class="text">
                          <p><strong>Lorem ipsum dolor sit amet consectetur adipisicing.</strong></p>
                          <p class="date">12:53 AM Dec 19th</p>
                      </div>
                  </div>
                  <div class="d-flex">
                      <img src="../assets/images/our-office-5-square.jpg" alt="">
                      <div class="text">
                          <p><strong>Lorem ipsum dolor sit amet consectetur adipisicing.</strong></p>
                          <p class="date">12:53 AM Dec 19th</p>
                      </div>
                  </div>
              </div>
              <div class="col">
                  <h6>RECENT COMMENTS</h6>
                  <div class="recent-comment">
                      <p class="new-comment"><i class="fa-solid fa-chevron-right"></i><strong>John Doe</strong> commented on <span>Lorem ipsum dolor sit amet.</span> </p>
                      <p class="date">12:53 AM Dec 19th</p>
                  </div>
                  <div class="recent-comment">
                      <p class="new-comment"><i class="fa-solid fa-chevron-right"></i><strong>John Doe</strong> commented on <span>Lorem ipsum dolor sit amet.</span> </p>
                      <p class="date">12:53 AM Dec 19th</p>
                  </div>
              </div>
              <div class="col">
                  <h6>CATEGORIES</h6>
                  <div class="categories">
                      <span> GADGETS</span>
                      <span>PHOTOGRAPHY</span>
                      <span>LIFESTYLE</span>
                      <span>FASHION</span>
                      <span>RECIPES</span>
                      <span>TRAVEL</span>
                      <span>BUINESS</span>
                      <span>ARCHITECTURE</span>
                      <span>REVEWS</span>
                      <span>SPORTS</span>
                      <span>VIDEOS</span>
                      <span>TECHNOLOGY</span>
                      <span>DESIGN</span>
                  </div>
              </div>
              </div>
          </div>
      </div>
      <div class="footer-bottom"></div>
  </footer>
</template>

<script>
export default {
name:'FooterComp'
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars.scss';

.footer-top{
    background-color: #212529;
    .cg-container{
        position: relative;
        margin-bottom: 50px;
        .etichetta{
        position: absolute;
        top: -20px;
        left: 0px;
        color: white;
        background-color: $primary-color;
        padding: 5px 10px;
        }
    }
    h6{
        color: white;
    }
    p{
        color: #777777;
    }
    img{
        width: 70px;
        height: 70px;
        border-radius: 50%;
        margin-right: 5px;
    }
    .recent-comment{
        & i ,& span{
        color: $primary-color;
    }
    .new-comment{
        color: white;
    }
    
    }
    .categories span{
        background-color: black;
        font-weight: bold;
        color: white;
        display: inline-block;
        margin: 5px;
        padding: 3px 2px;
        border-radius: 5px;
        font-size: 0.8rem;
    }
    .date{
        font-size: 0.8rem;
    }
    
}
</style>