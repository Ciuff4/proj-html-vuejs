<template>
  <header>
    <div class="top-header container-fluid">
        <div class="container d-flex align-items-center h-100">
            <span>Everything about Lifestyle,Travel and Gadgets!</span>
            <ul class="d-flex align-items-center m-0">
                <li><a href="#">SIGN IN</a></li>
                <li><a href="#">ABOUT US</a></li>
                <li><a href="#">CONTACT US</a></li>
                <li><a href="#">BUY NOW</a></li>
            </ul>

        </div>
    </div>
    <div class="middle-header container d-flex align-items-center">
        <div class="w-50">
            <img src="../assets/images/logo-default-slim.png" alt="logo">
        </div>
    </div>
    <div class="bottom-header container d-flex pb-3">
        <div class="bh-left">
            <nav>
                <ul class="m-0 align-items-center justify-content-between">
                    <li 
                    v-for="( item , index ) in NavbarItems" :key="`navbar(${index})`" >
                        <a 
                        @click="item.isActive =!item.isActive" :class="{ active : item.isActive}" href="#">{{item.name}}</a>
                     </li>
                    
                </ul>
            </nav>
        </div>
        <div class="bh-right d-flex  align-items-center justify-content-end">
            <input v-model="textToSearch" type="searchbar" placeholder="Cerca qui">
            <i class="fa-solid fa-magnifying-glass"></i>
        </div>
    </div>
  </header>
</template>

<script>
import HeaderNavbar from '../assets/data/HeaderNavbar'

export default {
name:'HeaderComp',
data(){
    return {
        NavbarItems: HeaderNavbar,
        textToSearch:"",
    }
}

}

</script>

<style lang="scss" scoped>
@import '../assets/style/vars.scss';
.top-header{
    height: 40px;
    position:fixed;
    top: 0;
    z-index: 999;
    background-color: $primary-color;
    color: white;
    span{
        font-size: 0.7rem;
    }
    li{
        padding-left: 8px;
        font-size: 0.7rem;
    }
}
.middle-header{
    height: 110px;
    margin-top: 40px;
    img{
        width: 20%;
    }
}
.bottom-header{
    .bh-left{
        width: 50%;
        a{
            color:#212529;
            font-weight: bold;
            &.active{
                color: $primary-color;
            }
        }
    }
    .bh-right{
        width: 50%;
        input{
            border: none;
            border-radius: 10px;
        }
        i{
            margin-left: -20px;
        }
    }
}
</style>