<script setup>
import AppHeader from './components/AppHeader.vue'
</script>

<template>

  <AppHeader></AppHeader>
  <div class="content"></div>

</template>

<style lang="scss">
@use './styles/general.scss' as *;
@use './styles/partials/mixins' as *;
@use './styles/partials/variables' as *;

.content {
  background-color: $black;
  min-height: 100px;
  width: 100%;
}
</style>
