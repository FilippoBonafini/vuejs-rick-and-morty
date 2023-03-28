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
  methods: {
    search() {
      axios.get('https://rickandmortyapi.com/api/character', {
        params: {
          name: store.searchKey,
          status: store.searchStatus
        }
      })
        .then((response) => {
          console.log(response)
          this.store.characters = response.data.results;
          this.store.charactersFound = response.data.results.length
        })
        .catch((error) => {
          console.log(error)
          this.store.characters = []
          this.store.charactersFound = 0
        }
        )
    },
    reset() {
      store.searchKey = ''
      store.searchStatus = ''
      this.search()
    }
  },
  created() {
    this.search()
  }
}
</script>

<!-- HTML -->
<template>
  <AppHeader />
  <AppMain @search="search" @reset="reset" />
  <AppFooter />
</template>

<!-- CSS  -->
<style lang="scss"></style>
