<template>
    <header>
        <nav>
            <div class="logo"><img src="..\image\Frame 85.svg"></div>
            <div class="menu-container" :class="{open:isActive}">
                <div class="menu" :class="{open:isActive}">
                    <NuxtLink>Репродукции</NuxtLink>
                    <NuxtLink>Новинки</NuxtLink>
                    <NuxtLink>О нас</NuxtLink>
                    <NuxtLink><img class="basket-but" src="..\image\Frame 217.svg"></NuxtLink>
                </div>
            </div>
            <div class="mobile-menu">
                <div class="burger-container">
                    <div @click="getClassStatus" class="burger" :class="{ active: isActive }"><span></span></div>
                </div>
                <div class="basket-container">
                    <NuxtLink><img class="basket-mobile" src="..\image\Frame 217.svg"></NuxtLink>
                </div>
            </div>
        </nav>
    </header>
    <slot />
    <footer></footer>
</template>
<style>
footer{background-color: #E1EDE6;height: 20.5vh;display: flex;}
header{background-color: #E1EDE6;height: 12.5vh;display: flex;flex-direction: column;justify-content: center;}
.logo {padding-left: 10%;width: 143px;height: 35px;}
.menu-container{width: 100%;display: flex;justify-content: flex-end;padding-right: 10%;}
.menu{width: 32vw;display: flex;align-items: center;font-family: Raleway;font-weight: 500;justify-content: space-between;font-size: 1.25rem;}
nav{display: flex;}
.burger {
    display: none;
    position: relative;
    z-index: 50;
    align-items: center;
    justify-content: flex-end;
    width: 30px;
    height: 18px;
}
.basket-mobile{display: none;}
.open{
    display: flex !important;
}
.burger span {
    height: 2px;
    width: 100%;
    transform: scale(1);
    background-color: #4C5866;
}
.burger::before, .burger::after{
    content: '';
    position: absolute;
    height: 2px;
    width: 100%;
    background: #4C5866;
    transition:all 0.3s ease 0s;
}
.burger::before {
    top: 0;
}

.burger::after {
    bottom: 0;
}
.burger.active span{transform: scale(0);}
.burger.active::before{
    top:50%;
    transform: rotate(-45deg) translate(0,-50%);
}
.burger.active::after{
    bottom: 50%;
    transform: rotate(45deg) translate(0,50%);
}
@media (max-width:1250px) {
    .menu {
        display: flex;
        width: 58vw;
        font-size: 1.125rem;
    }
    .menu-container{display: flex;padding-right: 5%;}
    .logo{padding-left: 5%;}
}
@media (max-width:690px) {
    .logo {display: block;padding: 0;margin: 0 auto;padding-bottom: 1.5vh;}
    .menu{display: flex;width: 85%;padding: 1.5vh 0 0 0;border-top:1px solid #C3D1C6;}
    .menu-container{display:flex;padding: 0;align-items: center;justify-content: center;}
    nav{display: block;}
    .basket-but{padding-left: 10vw;}
    header{height: 15vh;}
}
@media (max-width:400px){
    .basket-but{display: none;}
    .burger{display: flex;}
    .logo {display: block;padding: 0;margin: 0 auto;padding-bottom: 1.5vh;}
        .menu {
            padding-left: 4%;
            display: none;
            border: none;
            flex-direction: column;
            align-items: flex-start;
            height:20vh;
            width: 100%;
            height: 18vh;
            top: 0;
            bottom: 0;
            left: 0;
            right: 0;
            z-index: 50;
            overflow-y: auto;
            padding-top: 11vh;
            justify-content:space-between;
            font-size: 1.125rem;
            z-index: 50;
        }
        .menu-container{   display:none; position: fixed;height: 100%;width: 100%;
            background-color: #E1EDE6;align-items: flex-start;    z-index: 50;}
    header{height: 15vh;background-color: white;}
    .mobile-menu{display: flex; justify-content: space-between;background-color:#E1EDE6 ;height: 8vh;align-items: center;}
    .basket-container .basket-mobile{display: flex;}
    .basket-container{display: flex;width:auto;justify-content: end;padding-right: 5%;}
    .burger-container{padding-left: 5%;}
}
</style>
<script>
export default{
    data() {
        return{
            isActive:false,
            clickCount:0,
        }
    },
    methods:{getClassStatus(){
        if (this.isActive){
            this.isActive=false;
        }
        else {
            this.isActive=true;
            this.clickCount+=1;
        }
    }}
}
</script>