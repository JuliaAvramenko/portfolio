<script setup>
import Header from './Header.vue';
</script>

<template>
    <section class="top">
        <div class="top__container">
            <Header></Header>
            <img src="../assets/images/julia-min.jpg" alt="портрет" class="top__image">
            <!-- <img src="../assets/images/julia.jpg"  alt="портрет" class="top__image">        -->

            <div class="top__wrapper">
                <p class="top__text">Hello, I'm</p>
                <h1 class="top__title">Julia</h1>
                <h1 class="top__title"> Avramenko</h1>
                <p class="top__paragraph">Frontend Developer</p>
            </div>
        </div>
    </section>
</template>

<style scoped>
.top {
    display: flex;
    width: 100%;
    justify-content: center;

}

.top__container {
    display: flex;
    column-gap: 70px;
    background-color: #096766;
    position: relative;
    z-index: 1;
    min-width: 1000px;
    height: 600px;

}

@media (max-width: 1200px) {
    .top__container {
        min-width: 700px;
        height: 450px;
        column-gap: 40px;
    }
}

@media (max-width: 700px) {
    .top__container {
        min-width: 100%;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        height: 820px;
    }
}

.top__wrapper {
    display: flex;
    flex-direction: column;
    margin-top: 200px;
}

@media (max-width: 1200px) {
    .top__wrapper {
        margin-top: 130px;
    }
}

@media (max-width: 700px) {
    .top__wrapper {
        margin-top: 0;
        justify-content: center;
        align-items: center;
    }
}

.top__title {
    font-family: "Merriweather", sans-serif;
    margin: 0;
    padding: 0;
    font-weight: 600;
    font-size: 70px;
    color: rgb(255, 191, 0);
    margin-bottom: 50px;
    line-height: 30px;
}

@media (max-width: 1200px) {
    .top__title {
        font-size: 45px;
        line-height: 30px;
        margin-bottom: 25px;
    }
}

@media (max-width: 700px) {
    .top__title {
        font-size: 50px;
        line-height: 50px;
        margin-bottom: 0;
        margin-top: 0;

    }
}

.top__text {
    margin: 0;
    padding: 0;
    font-weight: 300;
    font-size: 40px;
    color: #4cc2de;
    margin-bottom: 80px;
    color: rgb(228, 226, 226);
}

@media (max-width: 1200px) {
    .top__text {
        font-size: 30px;
        margin-bottom: 60px;
    }
}

@media (max-width: 700px) {
    .top__text {
        font-size: 30px;
        margin-bottom: 30px;
    }
}

.top__paragraph {
    margin: 0;
    padding: 0;
    font-weight: 400;
    font-size: 30px;
    color: #4cc2de;
    margin-bottom: 50px;
    color: rgb(228, 226, 226);
}


@media (max-width: 1400px) {
    .top__paragraph {
        font-size: 25px;
        /* margin-top: 10px; */
    }
}

@media (max-width: 700px) {
    .top__paragraph {
        margin-top: 30px;
    }
}

.top__image {
    height: 100%;
    object-fit: contain;
}

@media (max-width: 700px) {
    .top__image {
        height: 450px;
        margin-right: 0;
        object-fit: contain;
        margin-top: 110px;
        margin-bottom: 30px;
        box-shadow: 10px 10px 5px 0px rgba(0, 0, 0, 0.4);
    }
}
</style>