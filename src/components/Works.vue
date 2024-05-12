<script setup>
import { ref } from 'vue';

const slides = ref([ 
// { url: '' },
// { url: '' }, 
// { url: '' },
{ url: 'https://juliaavramenko.github.io/react-nft-project/' },
{ url: 'https://juliaavramenko.github.io/decent-test-task/' }, 
{ url: 'https://juliaavramenko.github.io/forecast-vue-test-task/' }, 
{ url: 'https://juliaavramenko.github.io/go-scooter-pass/' },
{ url: 'https://juliaavramenko.github.io/ams-software-test-task/' }, 
{ url: 'https://juliaavramenko.github.io/burger-react-practicum/' },
{ url: 'https://juliaavramenko.github.io/house-hunter-react/' }, 
{ url: 'https://juliaavramenko.github.io/language-school/' },
{ url: 'https://juliaavramenko.github.io/it-studio/' },   
{ url: 'https://juliaavramenko.github.io/russian-travel-JUL-LIA/' },
{ url: 'https://juliaavramenko.github.io/practice-portfolio/' }, 
{ url: 'https://juliaavramenko.github.io/how-to-learn-bootcamp/' },
{ url: 'https://juliaavramenko.github.io/mesto-project-bootcamp/' },
{ url: 'https://juliaavramenko.github.io/burgers-angular/' },
]);

const currentSlide = ref(0);

const prevSlide = () => {
currentSlide.value = (currentSlide.value > 0) ? currentSlide.value - 1 : slides.value.length - 1;
};

const nextSlide = () => {
currentSlide.value = (currentSlide.value < slides.value.length - 1) ? currentSlide.value + 1 : 0;
};

</script>

<template>
<section class="works" id="works">    
    <div class="works__container">
        <h3 class="works__title">My projects</h3>   
        
        <div class="slider">
<div class="slides" :style="{ transform: `translateX(-${currentSlide * 100}%)` }">
<div class="slide" v-for="(slide, index) in slides" :key="index">
<!-- Ваш контент для слайда -->
<iframe :src="slide.url" 
    frameborder="0"
    scroll="none"   
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    allowFullScreen class="works__video" 
    seamless
></iframe>
</div>
</div>
<div class="buttons">
<button @click="prevSlide" class="button">Previous</button>
<button @click="nextSlide" class="button">Next</button>
</div>
</div>
                <!-- <div class="works__cards">
                    <article class="works__card1">
                        <a href="https://juliaavramenko.github.io/how-to-learn-bootcamp/" class="works__link"
                            target="_blank">
                            <img src="<%=require('./images/right-arrow.svg')%>" alt="" class="works__icon">
                        </a>
                        <iframe width="550px" height="500px" scroll="none"
                            src="https://juliaavramenko.github.io/how-to-learn-bootcamp/"
                            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                            allowFullScreen class="works__video1" seamless></iframe>
                    </article>

                    <article class="works__card2">
                        <a href="https://juliaavramenko.github.io/mesto-project-bootcamp/" class="works__link"
                            target="_blank">
                            <img src="<%=require('./images/right-arrow.svg')%>" alt="" class="works__icon">
                        </a>
                        <iframe width="550px" height="500px" scroll="none"
                            src="https://juliaavramenko.github.io/mesto-project-bootcamp/"
                            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                            allowFullScreen class="works__video2" seamless></iframe>

                    </article>
                    <article class="works__card3">
                        <a href="https://juliaavramenko.github.io/burgers-angular/" class="works__link" target="_blank">
                            <img src="<%=require('./images/right-arrow.svg')%>" alt="" class="works__icon">
                        </a>
                        <iframe width="550px" height="500px" scroll="none"
                            src="https://juliaavramenko.github.io/burgers-angular/"
                            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                            allowFullScreen class="works__video3" seamless></iframe>
                    </article>
                    <article class="works__card4">
                        <a href="https://juliaavramenko.github.io/practice-portfolio/" class="works__link"
                            target="_blank">
                            <img src="<%=require('./images/right-arrow.svg')%>" alt="" class="works__icon">
                        </a>
                        <iframe width="550px" height="500px" scroll="none"
                            src="https://juliaavramenko.github.io/practice-portfolio/"
                            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                            allowFullScreen class="works__video9"></iframe>
                    </article>
                    <article class="works__card5">
                        <a href="https://juliaavramenko.github.io/russian-travel-JUL-LIA/" class="works__link"
                            target="_blank">
                            <img src="<%=require('./images/right-arrow.svg')%>" alt="" class="works__icon">
                        </a>
                        <iframe width="550px" height="500px" scroll="none"
                            src="https://juliaavramenko.github.io/russian-travel-JUL-LIA/"
                            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                            allowFullScreen class="works__video5"></iframe>
                    </article>
                    <article class="works__card6">
                        <a href="https://juliaavramenko.github.io/it-studio/" class="works__link" target="_blank">
                            <img src="<%=require('./images/right-arrow.svg')%>" alt="" class="works__icon">
                        </a>
                        <iframe width="550px" height="500px" scroll="none"
                            src="https://juliaavramenko.github.io/it-studio/"
                            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                            allowFullScreen class="works__video6"></iframe>
                    </article>
                    <article class="works__card7">
                        <a href="https://juliaavramenko.github.io/language-school/" class="works__link" target="_blank">
                            <img src="<%=require('./images/right-arrow.svg')%>" alt="" class="works__icon">
                        </a>
                        <iframe width="550px" height="500px" scroll="none"
                            src="https://juliaavramenko.github.io/language-school/"
                            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                            allowFullScreen class="works__video7"></iframe>
                    </article>
                    <article class="works__card8">
                        <a href="https://juliaavramenko.github.io/house-hunter-react/" class="works__link"
                            target="_blank">
                            <img src="<%=require('./images/right-arrow.svg')%>" alt="" class="works__icon">
                        </a>
                        <iframe width="550px" height="500px" scroll="none"
                            src="https://juliaavramenko.github.io/house-hunter-react/"
                            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                            allowFullScreen class="works__video9"></iframe>
                    </article>
                    <article class="works__card9">
                        <a href="https://juliaavramenko.github.io/burger-react-practicum/" class="works__link"
                            target="_blank">
                            <img src="<%=require('./images/right-arrow.svg')%>" alt="" class="works__icon">
                        </a>
                        <iframe width="550px" height="500px" scroll="none"
                            src="https://juliaavramenko.github.io/burger-react-practicum/"
                            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                            allowFullScreen class="works__video9"></iframe>
                    </article> -->

                <!-- </div> -->
            </div>
        </section>
 
</template>

<style scoped>

.slider {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    position: relative;
    overflow: hidden;
}
.slides {
    display: flex;
    width: 900px;
    height: 400px;
    transition: transform 0.5s ease;
}

@media (max-width: 1200px) {
    .slides {
        width: 700px;
        height: 350px;
    }
}

@media (max-width: 700px) {
    .slides {
        width: 500px;
        height: 300px;
    }
}
.slide {
    min-width: 100%; 
    transition: transform 0.5s ease;
}
iframe {
 width: 550px;
 height: 500px;
}
.works__video {
    width: 200%;
    height: 200%;
    border: 0;    
    list-style-type: none;
    margin-bottom: 0;
    margin-top: 0;
    -o-object-fit: cover;
    object-fit: cover;
    overflow: hidden;
    padding-left: 0;
    transform: scale(0.5);
    transform-origin: 0 0;
    background-color: #fff;
}

@media (max-width: 1200px) {
    .works__video {
        width: 250%;
        height: 250%;
        transform: scale(0.4);
    }
}

@media (max-width: 700px) {
    .works__video {
        width: 400%;
        height: 400%;
        transform: scale(0.25);
    }
}

.buttons {
    display: flex;
    column-gap: 50px;
    margin-top: 30px;
}
.button {
    background-color: #002726;
    color: #ffffffcc;
    width: 130px;
    height: 40px;
    font-size: 18px;
    border-radius: 5px; /* Скругление углов */
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
.button:hover {
    opacity: 0.7;
}


.works {
    background-image: url(./../assets/images/coding.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    width: 100%;
    display: flex;
    flex-direction: column;
    position: relative;
    z-index: 2;
    padding-top: 50px;
    padding-bottom: 50px;    
}

.works::before {
    width: 100%;
    height: 100%;
    z-index: -1;
    left: 0;
    top: 0;
    position: absolute;
    content: "";
    background-color: rgba(228, 226, 226, 0.484);
    opacity: 0.7;
}


.works__container {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.works__title {
    font-family: "Gilroy-Semibold", sans-serif;
    margin: 0;
    padding: 0;
    font-weight: 600;
    font-size: 60px;  
    color: #002726;
    margin-bottom: 30px;    
}

@media (max-width: 1200px) {
    .works__title {
        font-size: 50px;
    }
}

@media (max-width: 700px) {
    .works__title {
        font-size: 40px;
        margin-bottom: 20px;
    }
}



</style>