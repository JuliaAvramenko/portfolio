<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const animatedElement = ref(null);
const isIntersecting = ref(false);

const observer = new IntersectionObserver(
    ([entry]) => {
        isIntersecting.value = entry.isIntersecting;
        if (entry.isIntersecting) {
            entry.target.style.animation = 'none';
            entry.target.offsetHeight;
            entry.target.style.animation = null;
        }
    },
    { threshold: 0.5 }
);

onMounted(() => {
    observer.observe(animatedElement.value);
});

onUnmounted(() => {
    observer.disconnect();
});

</script>

<template>
    <section class="about" id="about">
        <div class="about__container">
            <h2 class="about__title">About me</h2>
            <p class="about__text">I am a passionate Junior Frontend Developer. I can develop a landing page within
                a couple of days. I'm really into what I'm doing. Your dreams will come true with me!</p>
            <h2 class="about__title">My stack</h2>
            <div class="icons">
                <img src="../assets/icons/html.svg" alt="html" :class="{ 'animate': isIntersecting }"
                    ref="animatedElement" class="icon">
                <img src="../assets/icons/css.svg" alt="css" :class="{ 'animate': isIntersecting }"
                    ref="animatedElement" class="icon">
                <img src="../assets/icons/js.svg" alt="js" :class="{ 'animate': isIntersecting }" ref="animatedElement"
                    class="icon">
                <img src="../assets/icons/github.svg" alt="github" :class="{ 'animate': isIntersecting }"
                    ref="animatedElement" class="icon">
                <img src="../assets/icons/react.svg" alt="react" :class="{ 'animate': isIntersecting }"
                    ref="animatedElement" class="icon">
                <img src="../assets/icons/typescript.svg" alt="typescript" :class="{ 'animate': isIntersecting }"
                    ref="animatedElement" class="icon">
                <img src="../assets/icons/redux.svg" alt="redux" :class="{ 'animate': isIntersecting }"
                    ref="animatedElement" class="icon">
                <img src="../assets/icons/toolkit.svg" alt="toolkit" :class="{ 'animate': isIntersecting }"
                    ref="animatedElement" class="icon">
                <img src="../assets/icons/api.svg" alt="api" :class="{ 'animate': isIntersecting }"
                    ref="animatedElement" class="icon">
                <img src="../assets/icons/storybook.svg" alt="storybook" :class="{ 'animate': isIntersecting }"
                    ref="animatedElement" class="icon">
                <img src="../assets/icons/webpack.svg" alt="webpack" :class="{ 'animate': isIntersecting }"
                    ref="animatedElement" class="icon">
                <img src="../assets/icons/figma.svg" alt="figma" :class="{ 'animate': isIntersecting }"
                    ref="animatedElement" class="icon">
                <img src="../assets/icons/responsive.svg" alt="responsive" :class="{ 'animate': isIntersecting }"
                    ref="animatedElement" class="icon">
                <img src="../assets/icons/bootstrap.svg" alt="bootstrap" :class="{ 'animate': isIntersecting }"
                    ref="animatedElement" class="icon">
                <img src="../assets/icons/vue.svg" alt="vue" :class="{ 'animate': isIntersecting }"
                    ref="animatedElement" class="icon">
                <img src="../assets/icons/bem.svg" alt="bem" :class="{ 'animate': isIntersecting }"
                    ref="animatedElement" class="icon">
                <img src="../assets/icons/scss.svg" alt="scss" :class="{ 'animate': isIntersecting }"
                    ref="animatedElement" class="icon">
                <img src="../assets/icons/tailwind.svg" alt="tailwind" :class="{ 'animate': isIntersecting }"
                    ref="animatedElement" class="icon">
                <img src="../assets/icons/vite.svg" alt="vite" :class="{ 'animate': isIntersecting }"
                    ref="animatedElement" class="icon">
                <img src="../assets/icons/postman.svg" alt="postman" :class="{ 'animate': isIntersecting }"
                    ref="animatedElement" class="icon">
            </div>
        </div>

    </section>
</template>


<style scoped>
.about {
    width: 100%;
    background-color: rgba(207, 190, 190, 0.473);
    padding-top: 50px;
    padding-bottom: 50px;
}

.about__container {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    max-width: 900px;
    margin-left: auto;
    margin-right: auto;
}

@media (max-width: 1400px) {
    .about__container {
        max-width: 800px;
    }
}

@media (max-width: 700px) {
    .about__container {
        max-width: 500px;
    }
}

.about__title {
    font-family: "Gilroy-Semibold", sans-serif;
    margin: 0;
    padding: 0;
    font-weight: 600;
    font-size: 60px;
    color: #007472;
    margin-bottom: 30px;
}

@media (max-width: 1200px) {
    .about__title {
        font-size: 50px;
        margin-bottom: 30px;
    }
}

@media (max-width: 700px) {
    .about__title {
        font-size: 40px;
        margin-bottom: 20px;
    }
}

.about__text {
    color: hsla(0, 3%, 6%, 0.823);
    font-size: 30px;
    font-weight: 400;
    line-height: 50px;
    margin: 0 50px 50px;
    padding: 0;
    text-align: center;

}

@media (max-width: 1400px) {
    .about__text {
        font-size: 25px;
        line-height: 35px;
    }
}

@media (max-width: 700px) {
    .about__text {
        font-size: 20px;
        margin-bottom: 30px;
        line-height: 35px;
        display: flex;
        justify-content: center;
        gap: 10px;
        flex-wrap: wrap;
    }
}



.icons {
    display: flex;
    gap: 20px;
    flex-wrap: wrap;
    width: 700px;
}

@media (max-width: 1200px) {
    .icons {
        justify-content: center;
    }
}

@media (max-width: 700px) {
    .icons {
        column-gap: 10px;
        row-gap: 20px;
        width: 500px;

    }
}

@media (max-width: 500px) {
    .icons {
        width: 400px;
    }
}

.icon {
    width: 50px;
    height: 50px;
    opacity: 0;

}

.animate {
    animation: snake-and-grow 2s ease-in forwards;
}


@keyframes snake-and-grow {
    0% {
        opacity: 0;
        transform: translateX(-20px) scale(0);
    }

    50% {
        opacity: 1;
        transform: translateX(0px) scale(1.2);
    }

    100% {
        opacity: 1;
        transform: translateX(0) scale(1);
    }
}

.icon:nth-child(1) {
    animation-delay: 0s;
}

.icon:nth-child(2) {
    animation-delay: 0.5s;
}

.icon:nth-child(3) {
    animation-delay: 1s;
}

.icon:nth-child(4) {
    animation-delay: 1.5s;
}

.icon:nth-child(5) {
    animation-delay: 2s;
}

.icon:nth-child(6) {
    animation-delay: 2.5s;
}

.icon:nth-child(7) {
    animation-delay: 3s;
}

.icon:nth-child(8) {
    animation-delay: 3.5s;
}

.icon:nth-child(9) {
    animation-delay: 4s;
}

.icon:nth-child(10) {
    animation-delay: 4.5s;
}

.icon:nth-child(11) {
    animation-delay: 5s;
}

.icon:nth-child(12) {
    animation-delay: 5.5s;
}

.icon:nth-child(13) {
    animation-delay: 6s;
}

.icon:nth-child(14) {
    animation-delay: 6.5s;
}

.icon:nth-child(15) {
    animation-delay: 7s;
}

.icon:nth-child(16) {
    animation-delay: 7.5s;
}

.icon:nth-child(17) {
    animation-delay: 8s;
}

.icon:nth-child(18) {
    animation-delay: 8.5s;
}

.icon:nth-child(19) {
    animation-delay: 9s;
}

.icon:nth-child(20) {
    animation-delay: 9.5s;
}
</style>