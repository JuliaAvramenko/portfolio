<script setup>

</script>

<template>
    <footer class="footer" id="contact">
        <div class="footer__container">
            <div class="footer__info">
                <h2 class="footer__title">Contact me</h2>
                <div class="footer__wrapper">
                    <img src="../assets/images/phone.png" alt="" class="footer__icon">
                    <a href="tel:+79166912742" class="footer__link" target="_blank">
                        <p class="footer__text"><span class="footer__span">Tel.:</span> +7 (916) 691-27-42</p>
                    </a>
                </div>
                <div class="footer__wrapper">
                    <img src="../assets/images/envelope.png" alt="" class="footer__icon">
                    <a href="mailto:miraclejuliet@yandex.ru" class="footer__link" target="_blank">
                        <p class="footer__text"><span class="footer__span">E-mail: </span>miraclejuliet@yandex.ru
                        </p>
                    </a>
                </div>
                <div class="footer__wrapper">
                    <img src="../assets/images/telegram.svg" alt="" class="footer__icon">
                    <a href="https://t.me/lia_jul_07" class="footer__link" target="_blank">
                        <p class="footer__text"><span class="footer__span">Telegram: </span>@lia_jul_07</p>
                    </a>
                </div>

                <div class="footer__wrapper">
                    <img src="../assets/images/linkedin.svg" alt="" class="footer__icon">

                    <a href="https://www.linkedin.com/in/avramenko-yulia" class="footer__link" target="_blank">
                        <p class="footer__text"><span class="footer__span">LinkedIn:</span> Get in touch
                        </p>
                    </a>
                </div>

                <div class="footer__wrapper">
                    <img src="../assets/images/github.svg.png" alt="" class="footer__icon">
                    <a href="https://github.com/JuliaAvramenko" class="footer__link" target="_blank">
                        <p class="footer__text"><span class="footer__span">GitHub:</span> Look at my works
                        </p>
                    </a>
                </div>


            </div>

            <img src="../assets/images/jul2.jpg" data-src="TODO" alt="аватар" class="footer__image">


        </div>
    </footer>
</template>

<style scoped>
.footer {
    display: flex;
    justify-content: center;
    width: 100%;
}

.footer__container {
    display: flex;
    column-gap: 130px;
    justify-content: center;
    background-color: #096766;
    padding: 50px;
    min-width: 900px;
}

@media (max-width: 1200px) {
    .footer__container {
        min-width: 700px;
        column-gap: 30px;
        align-items: center;
        padding-right: 0;
        padding-left: 0;
    }
}


@media (max-width: 700px) {
    .footer__container {
        min-width: 100%;
        flex-direction: column;
        justify-content: center;

    }
}

.footer__wrapper {
    display: flex;
    align-items: center;
    column-gap: 30px;
}

@media (max-width: 1200px) {
    .footer__wrapper {
        column-gap: 15px;
    }
}

.footer__title {
    font-family: "Gilroy-Semibold", sans-serif;
    margin: 0;
    padding: 0;
    font-weight: 600;
    font-size: 65px;
    color: rgb(255, 191, 0);
    margin-bottom: 30px;
}

@media (max-width: 1400px) {
    .footer__title {
        font-size: 50px;
        margin-bottom: 10px;
    }
}

@media (max-width: 700px) {
    .footer__title {
        font-size: 40px;
        line-height: 40px;
        text-align: center;
    }
}

.footer__text {
    margin: 0;
    padding: 0;
    font-weight: 300;
    font-size: 25px;
}

@media (max-width: 1200px) {
    .footer__text {
        font-size: 20px;
    }
}

@media (max-width: 700px) {
    .footer__text {
        font-size: 18px;
        text-decoration: none;
    }
}

.footer__span {
    font-family: "Gilroy-Semibold", sans-serif;
    font-weight: 600;
    font-size: 20px;
    color: rgb(228, 226, 226);
    color: #002726;
}

@media (max-width: 1200px) {
    .footer__span {
        font-weight: 600;
        font-size: 16px;
    }
}

@media (max-width: 700px) {
    .footer__span {
        font-weight: 600;
        font-size: 20px;
    }
}

.footer__link {
    text-decoration: none;
    color: rgb(228, 226, 226);
}

.footer__link:hover {
    text-shadow: 1px 1px 1px black;
    color: rgb(255, 191, 0);
    opacity: 0.7;
}

.footer__info {
    display: flex;
    flex-direction: column;
    row-gap: 25px;
}

@media (max-width: 700px) {
    .footer__info {
        margin-left: 0;
        margin-top: 0;
        row-gap: 15px;
        margin-bottom: 30px;
    }
}


.footer__image {
    display: flex;
    border-radius: 50%;
    object-fit: cover;
    width: 40%;
    height: 400px;
    box-shadow: 10px 10px 5px 0px rgba(0, 0, 0, 0.4);
}

@media (max-width: 1200px) {
    .footer__image {
        height: 300px;
        width: 280px;
    }
}

.footer__icon {
    width: 30px;
    height: 30px;
}

@media (max-width: 700px) {
    .footer__icon {
        width: 20px;
        height: 20px;
    }
}
</style>