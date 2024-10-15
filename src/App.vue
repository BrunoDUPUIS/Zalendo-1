<script setup>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Details from './components/Details.vue'
import productInfo from './assets/data.json'
</script>

<template>
  <div>
    <Header />
    <main>
      <!-- wrapper -->
      <div class="container">
        <!-- 1ère colonne -->
        <div><!-- future image --></div>
        <!-- 2ème colonne -->

        <Details :productInfo="productInfo" />
        <!-- le composant Details remplace l'ancienne structure qui a été transféré dans Details -->
      </div>
    </main>
    <Footer />
  </div>
</template>

<style scoped>
* {
  box-sizing: border-box;
}
.container {
  display: flex;
  height: calc(
    100vh - var(--header-top-heigth) - var(--header-bottom-heigth) -
      var(--footer-heigth)
  );
}
.container > div {
  width: 50%;
  border: 1px solid green;
}
.container > div:last-child {
  padding: 25px 0 25px 100px;
}
/* la suite du CSS a été tranféré dans le composant Details */
</style>
