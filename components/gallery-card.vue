<template>
    <div class="minicard-container">
        <div class="wrapper-card"><img src="..\image\3004b7d8a3c0e2de1caa8fd5732848be.jpg">
            <div class="author-container">
                <p>Марсель Руссо</p>
            </div>
            <div class="name-container">
                <p>Охота Амура</p>
            </div>
            <div class="parametr-container">
                <p>Холст, масло (50х80) </p>
            </div>
            <div class="price-container">
                <p>14 500 руб</p>
            </div>
            <div class="button-inbasket"><button>В корзину</button></div>
        </div>
    </div>
</template>
<style>
.minicard-container{padding-bottom: 3%;}
.button-inbasket{display: flex;justify-content: center; padding-top:5% ;}
.button-inbasket button{padding:1.5rem 7.8rem;color: #598D66;background: transparent;border: #598D66 solid 1px;}
.price-container{
    font-family: Raleway;
    font-weight: 500;
    font-size: 1.5rem;
    color: #598D66;
    padding-left: 5%;
    padding-top: 8%;
}
.parametr-container {
    font-size: 1.125rem;
    font-family: Raleway;
    font-weight: 500;
    padding-left: 5%;
    padding-top:1% ;
}

.name-container {
    padding-left: 5%;
    padding-top: 2%;
    font-family: Raleway;
    font-size: 1.875rem;
    font-weight: 500;
    color: #2C2D35
}

.author-container {
    padding-left: 5%;
    padding-top: 5%;
    font-family: Raleway;
    font-size: 1.125rem;
    font-weight: 500;
    color: #86928B;
}

.wrapper-card {
    width: 350px;
    height: 730px;
    background-color: #E1EDE6;
    display: flex;
    flex-direction: column;
}

.wrapper-card img {
    width: 90%;
    height: 60%;
    margin: 0 auto;
    padding-top: 5%;
}
</style>