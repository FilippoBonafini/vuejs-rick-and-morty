<!-- JAVA SCRIPT  -->
<script>
// IMPORTIAMO COMPONENTI 
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import axios from 'axios';
import { store } from './store';

export default {
  name: 'App',
  // DICHIARIAMO I COMPONENTI 
  components: {
    AppHeader,
    AppMain,
    AppFooter,
  },
  data() {
    return {
      store
    }
  },
  created() {
    axios.get('https://rickandmortyapi.com/api/character')
      .then((response) => {
        console.log(response)
        this.store.characters = response.data.results;
        this.store.charactersFound = response.data.results.length
      })
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
