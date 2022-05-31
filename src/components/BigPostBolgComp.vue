<template>
  <div class="post">
      <img class="w-100 pb-3" src="../assets/images/blog-55 (1).jpg" alt="">
      <div class="d-flex">
          <div class="day d-flex flex-column mt-3 me-3">
              <span class="day-published">12</span>
              <span class="month-published">jan</span>
          </div>
          <div class="post-text">
              <h4>titolo</h4>
              <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate labore magni dolorem in sed incidunt libero, eligendi neque pariatur doloremque numquam, qui minus enim veritatis repellendus sequi ea porro veniam dicta fugiat! Dolorum totam, ut blanditiis enim odit cumque molestiae.</p>
              <div class="post-info d-flex ">
                  <div class="post-info-sx d-flex justify-content-around w-50">
                      <div>
                        <i class="fa-solid fa-user"></i>
                        <span>by John Doe</span>
                      </div>
                      <div>
                        <i class="fa-solid fa-folder"></i>
                        <span>lifestyle , travel</span>
                      </div>
                      <div>
                        <i class="fa-solid fa-comment"></i>
                        <span> 12 comments</span>
                      </div>
                  </div>
                  <div class="post-info-dx d-flex justify-content-end w-50">
                      <button type="button" class="btn btn-outline-secondary btn-sm">READ MORE</button>
                  </div>
              </div>
          </div>
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.post{
    height: 250px;
    .day span{
        width: 40px;
        
        font-weight: bold;
        margin: 0 auto;
        &.day-published{
            padding: 15px;
            background-color: #F7F7F7;
            color: #212529;
        }
        &.month-published{
            padding: 0px 15px;
            background-color: #212529;
            color:#F7F7F7 ;
            font-size: 0.7rem;
        }
        
    }
    p{
        color: #B7B7B7;
    }
    .post-info-sx{
        font-size: 0.9rem;
        color: #B7B7B7;
        i{
            padding-right: 5px;
        }
    }
}
</style>