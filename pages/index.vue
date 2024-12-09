<template>
    <div class="main-screen">
        <div class="main-screen__image-wrapper"><img src="..\image\767b0d204fdcdde61134fd1d03c4e51a (1).png"></div>
        <div class="title-container">
            <div class="main-screen__about-corp">
                <h1>Реплики картин <br> от <span>Ink. House</span></h1>
            </div>
            <div class="main-screen__min-info">
                <p>Высокое качество отрисовки на плотной бумаге или льняном <br> холсте. Редкие произведения, доступные
                    цены.</p>
            </div>
        </div>
    </div>
    <div class="reproduction-title">
        <h2>Репродукции</h2>
        <div class="filter-button"> <button style="background: #376B44;">Франция</button><button
                style="color: black;font-weight: 500;">Германия</button><button
                style="color: black; font-weight: 500;">Англия</button></div>
    </div>
    <div class="card-container">
        <GalleryCard v-for="n of 9" :key="n" />
    </div>
    <div class="new-collection">
        <div class="title-collection">
            <img src="..\image\Star 2.png">
            <p>Новая коллекция <br> французских авторов</p>
        </div>
        <div class="title-disc"><p>Сложно сказать, почему акционеры крупнейших компаний <br> призывают нас к новым
            свершениям, которые, в свою очередь,<br> должны быть заблокированы в рамках своих собственных
            <br>рациональных ограничений.</p><br>
            <p> Принимая во внимание показатели успешности,<br> граница обучения кадров предопределяет высокую
            востребованность <br>
            направлений прогрессивного развития.</p>
        </div>
        <div class="button-follow"><button>Ознакомиться</button></div>
    </div>
    <br><br><br><br><br><br><br><br><br><br>
</template>
<style>
body,html{margin: 0;padding: 0;background-color: #F4F6F5;}
.button-follow{padding-left: 10%;padding-top:3.5vh;padding-bottom: 5%;}
.button-follow button{color: #2C2D35;background: #EEDB6D; border: none;padding: 1.6rem 4rem;font-size: 1.25rem;}
.title-disc{font-family: Raleway;font-size: 1.125rem;color: white;padding-left: 10%;padding-top: 1%;}
.title-collection img{height: 7.5vh;width: 7.5vh;}
.title-collection{font-family: Raleway;font-size: 2.5rem;color: white;display: flex;align-items: center;padding-left: 10%;padding-top: 5%;}
.new-collection {
    height: 53vh;
    background: linear-gradient(to right, rgba(0, 0, 0, 0.6) 0%, rgba(0, 0, 0, 0.6) 29%, rgba(0, 0, 0, 0.04) 54%, rgba(0, 0, 0, 0) 57%), url("../image/6bcdb356971fca2ed6a45d666fd368a5.jpg");
    background-position: 100% 25%;
    background-size: cover;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
}
.title-container{display: flex;flex-direction: column; justify-content: center;height: 60vh;}
.main-screen__image-wrapper img{height: 70vh;transform: scale(-1, 1)}
.main-screen__image-wrapper{padding-left: 10%;display: flex;}
.main-screen__about-corp{color: #2C2D35;}
h1{font-size: 3.75rem;font-family: Raleway;font-weight: 500;}
h2{font-family: Raleway;font-weight: 500;font-size: 2.5rem;margin: 0;}
.main-screen__about-corp span {color: #598d66;}
.main-screen__min-info{display: flex;font-size: 1.125rem;font-family: Raleway;color: #86928B;padding-top: 1.5vh;}
p,h1{margin: 0;}
.main-screen{display: flex;}
.reproduction-title{padding-left: 10%;display: flex;justify-content: space-between;padding-right: 10%;}
.filter-button button{border-radius: 20px;background: #D4E8D9;color: white;font-family: Raleway;font-size: 1.25rem;border: none;padding:  0.625rem 1.5rem 0.625rem 1.5rem;}
.filter-button {display: flex;justify-content: space-between;width: 40%;}
.card-container{padding: 5% 10% 5% 10%;display: flex; flex-wrap: wrap;justify-content: space-between;}
</style>