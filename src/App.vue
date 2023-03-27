<!-- JAVA SCRIPT  -->
<script>
// IMPORTIAMO COMPONENTI 
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  name: 'App',
  // DICHIARIAMO I COMPONENTI 
  components: {
    AppHeader,
    AppMain,
    AppFooter
  }
}
</script>

<!-- HTML -->
<template>
  <AppHeader />
  <AppMain />
  <AppFooter />
</template>

<!-- CSS  -->
<style lang="scss"></style>
