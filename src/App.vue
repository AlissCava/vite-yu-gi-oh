<script>
import AppHeader from './components/AppHeader.vue'
import CharactersList from './components/CharactersList.vue'

export default {
  components: {
    AppHeader,
    CharactersList,
  }
}
</script>

<template>
  <AppHeader />
  <CharactersList />
  
</template>

<style lang="scss">
  #app {
    width: 100%;
    height: 100%;
    // border: 2px solid #8B4513; /* Cornice ocra */
    background-color: white;   /* Sfondo bianco */
    padding: 20px;
    box-sizing: border-box;
  }
</style>
