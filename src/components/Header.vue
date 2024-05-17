<script setup>

</script>

<template>
    <header class="header">
        <nav class="header__menu">
            <ul class="header__list">
                <li class="header__item"> <a href="#about" class="header__link">About me</a>
                </li>
                <li class="header__item"> <a href="#works" class="header__link">My works</a>
                </li>
                <li class="header__item"> <a href="#contact" class="header__link">Contact</a>
                </li>
            </ul>
        </nav>
    </header>

</template>

<style scoped>
.header {
    display: flex;
    flex-direction: column;
    position: absolute;
    top: 40px;
    right: 50px;
    z-index: 2;
}

@media (max-width: 1200px) {
    .header {
        right: 50px;

    }
}

@media (max-width: 700px) {
    .header {
        position: relative;
        top: 80px;
        right: 0px;
    }
}

.header__menu {
    margin: 0;
    padding: 0;
    display: flex;
    width: 300px;
    align-items: center;
    justify-content: space-between;
}

@media (max-width: 1200px) {
    .header__menu {
        width: 250px;
    }
}

@media (max-width: 700px) {
    .header__menu {
        width: 300px;
    }
}

.header__list {
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: space-between;
    width: 350px;
}

.header__link {
    text-decoration: none;
    color: rgb(228, 226, 226);
}

.header__link:hover {
    text-shadow: 1px 1px 1px black;
    color: rgb(255, 191, 0);
    opacity: 0.7;
    /* color: rgb(182, 179, 179); */
}

.header__item {
    margin: 0;
    padding: 0;
    font-weight: 400;
    font-size: 20px;
    list-style-type: none;
}

@media (max-width: 1200px) {
    .header__item {
        font-size: 15px;
    }
}

@media (max-width: 700px) {
    .header__item {
        font-size: 20px;
    }
}
</style>