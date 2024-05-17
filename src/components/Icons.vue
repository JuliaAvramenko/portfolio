<script setup>

</script>

<template>
   <section class="icons">
        <a href="https://t.me/lia_jul_07" class="icons__link" target="_blank">
            <img src="../assets/images/telegram_black.png" alt="telegram" class="icons__icon"></a>
        <a href="https://www.linkedin.com/in/avramenko-yulia" class="icons__link" target="_blank">
            <img src="../assets/images/linkedin.svg" alt="linkedin" class="icons__icon"></a>
        <a href="https://github.com/JuliaAvramenko" class="icons__link" target="_blank">
            <img src="../assets/images/github.svg.png" alt="github" class="icons__icon"></a>
    </section>
</template>

<style scoped>
.icons__icon {
    width: 50px;
    height: 50px;
}

.icons__icon:hover {
    background-color: #096766;
    opacity: 0.8;
}

@media (max-width: 1200px) {
    .icons__icon {
        width: 40px;
        height: 40px;
    }
}

@media (max-width: 700px) {
    .icons__icon {
        width: 20px;
        height: 20px;
    }
}

.icons {
    width: 60px;
    height: 240px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background-color: #ffbf00;
    position: fixed;
    z-index: 9;
    top: 250px;
    right: 0;
    row-gap: 30px;
}


@media (max-width: 1200px) {
    .icons {
        height: 200px;
        right: 0;
        row-gap: 20px;
        top: 180px;
        width: 60px;
    }
}

@media (max-width: 850px) {
    .icons {
        display: none;       
    }
}

</style>