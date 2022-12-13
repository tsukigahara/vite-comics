<script setup>
import AppHeader from './components/AppHeader.vue'
import AppFooter from './components/AppFooter.vue'
import linkInfo from './assets/dc-comics_links.json'
import cardInfo from './assets/dc-comics.json'
</script>

<template>
  <AppHeader :links="linkInfo[0].subitem" />
  <main>
    <div class="content">
      content here
    </div>
  </main>
  <AppFooter :links="linkInfo" />
</template>

<style lang="scss">
@use './styles/general.scss' as *;
@use './styles/partials/mixins' as *;
@use './styles/partials/variables' as *;

.content {
  text-align: center;
  line-height: 100px;
  background-color: $black;
  min-height: 100px;
  width: 100%;
  padding: 0 100px;
  color: white;
}
</style>
