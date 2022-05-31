<template>
  <section>
    <h6>FEATURED POSTS</h6>
    <div class="immagine">
        <img src="../assets/images/blog-66.jpg" alt="">
        <div class="overlay">
          <div class="text-overlay">
              <span>recipe</span>
              <h6>simple ways to have a pretty face</h6>
          </div>
        </div>
    </div>
    <h6>FEATURED AUTHOR</h6>
    <div class="author d-flex">
        <img src="../assets/images/avatar.jpg" alt="">
        <div class="about-author">
            <h6>John Doe</h6>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Veritatis, explicabo rerum labore nulla esse distinctio necessitatibus velit!</p>
        </div>
    </div>
  </section>
</template>

<script>
export default {
name:'FeaturedPosts'
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars.scss'; 
section{
    width: calc(100% / 3);
    .immagine{
    position: relative;
    width: 90%;
    height: 180px;
    img{
        width:100%;
        height:100%;
    }
    .overlay{
        position:absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        color: white;
        background-color: rgba(0, 0, 0, 0.171);
        &:hover{
            background-color: transparent;
        }
        .text-overlay{
            position:absolute;
            bottom: 13px;
            left: 13px;
            span{
                background-color: $primary-color;
                border-radius: 5px;
                padding: 0px 7px;
                font-size: 0.9rem;
            }
            h6{
                text-transform: capitalize;
            }
        }
    
    }
}
.author{
    margin-top: 15px;
    img{
        width: 100px;
        height: 100px;
        margin-right: 15px;
    }
    h6{
    font-weight: bold;
    }
    p{
        color: #B7B7B7;
        font-size: 0.9rem;
    }
}

}


</style>