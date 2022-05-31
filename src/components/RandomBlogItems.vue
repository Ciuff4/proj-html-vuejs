<template>
  <section>
      <div class="container pt-4">
          <div class="row row-cols-3">
              <div
              v-for="(article , index) in articles" :key="`article-${index}`"
              class="col d-flex justify-content-center pb-4">
                  <div class="immagine">
                      <img :src="article.image" alt="">
                      <div class="overlay">
                        <div class="text-overlay">
                            <span>{{article.tag}}</span>
                            <h6>{{article.title}}</h6>
                        </div>
                      </div>
                  </div>
              </div>
          </div>
      </div>
  </section>
</template>

<script>
import articles from '../assets/data/article'
export default {
name:'RandomBlogItems',
data(){
    return{
        articles:articles
    }
}
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars.scss';

section{
    background-color: #F7F7F7;
    .col{
        .immagine{
            position: relative;
            width: 90%;
            height: 180px;
            img{
                max-width:100%;
                max-height:100%;
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
    }
}
</style>