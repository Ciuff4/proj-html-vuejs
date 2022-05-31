<template>
  <div class="footer-bottom ">
      <div class="container d-flex justify-content-between align-items-center h-100">
          <div>
          <img src="../assets/images/logo-footer.png" alt="">
          <span>
              <i class="fa-solid fa-copyright"></i>
              Copyright 2020. All Rights Reserved.
            </span>
      </div>
      <div>
          <span>
              <i class="fa-solid fa-chevron-right"></i>
              FAQ's
          </span>
          <span>
              <i class="fa-solid fa-chevron-right"></i>
              Sitemap
          </span>
          <span>
              <i class="fa-solid fa-chevron-right"></i>
              Contact Us
          </span>
      </div>
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.footer-bottom{
    height: 80px;
    background-color: #1C2023;
    color: #777777;
    img{
        width: 100px;
        filter: brightness(70%);
        padding-right: 10px;
    }
    span{
        font-size: 0.7rem;
    }
}
</style>