<script setup>
//////////// import components //////////////
import AppHeader from './components/AppHeader.vue'
import AppFooter from './components/AppFooter.vue'
import AppCards from './components/AppCards.vue'

//////////// import json ///////////////////

// json, array of obj, linklist for AppHeader and AppFooter
import linkInfo from './assets/dc-comics_links.json'

// json array of obj for AppCards card
import cardInfo from './assets/dc-comics.json'
</script>

<template>
  <!-- header -->
  <AppHeader :links="linkInfo" />
  <main>
    <!-- content -->
    <AppCards :links="cardInfo" />
  </main>
  <!-- footer -->
  <AppFooter :links="linkInfo" />
</template>



<!-- how to props -->
<!-- set a props name in tag like :namehere="here imported json name" then go to components and declare in props:{} what type is your data(Array Object String Value etc.)-->


<style lang="scss">
// import scss
@use './styles/general.scss' as *;
@use './styles/partials/mixins' as *;
@use './styles/partials/variables' as *;
</style>
