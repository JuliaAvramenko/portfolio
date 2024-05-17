<script setup>
import About from './components/About.vue';
import Footer from './components/Footer.vue';
import Icons from './components/Icons.vue';
import Top from './components/Top.vue';
import Works from './components/Works.vue';

</script>

<template>
  <div class="container">
    <main class="pages">
      <Icons></Icons>
      <Top></Top>
      <About></About>
      <Works></Works>
      <Footer></Footer>
    </main>
  </div>

</template>

<style scoped>
.container {
  font-family: "Gilroy-Light", sans-serif;
  margin-top: 0;
  margin-bottom: 0;
  margin-left: auto;
  margin-right: auto;
  scroll-behavior: smooth;

}
</style>
