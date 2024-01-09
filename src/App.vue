<script>
// importo axios
import axios from 'axios';
//importo componenti figli
import AppHeader from './components/AppHeader.vue'
import CharactersList from './components/CharactersList.vue'
//importo lo store
import {store} from './store.js'

export default {
  components: {
    AppHeader,
    CharactersList,
  },

    data() {
      return {
        store,
    }
  }, 

  methods: {
    getCharacters() {
      axios
        .get(store.apiURL)
        .then ((res => {
          console.log (res.data.data);
          store.CharactersList = res.data.data;
        }))
        .catch((err) => {
          console.log ("Errori", err);
        });
     }
  },
  created() {
    this.getCharacters();
  }
};

</script>

<template>
  <AppHeader />
  <CharactersList />
  
</template>

<style lang="scss">
</style>
