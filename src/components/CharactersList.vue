<script>
import SingleCharacter from './SingleCharacter.vue'

//importo lo store
import {store} from '../store.js'

    export default {
        name: 'CharactersList',
        components: {
            SingleCharacter
        },

        data() {
            return {
                store,
        }
    }
}
</script>

<template>
    <section class="container">

        <div class="row">
            <!-- prototipo da ripetere -->
            <div v-for="card in store.CharactersList" :key="card.id"  class="col">
                <SingleCharacter />
            </div>
           
           
           

        </div>

    </section>
</template>

<style lang="scss" scoped>

.row{
    width: 100%;
    display: flex;
    flex-wrap: wrap;
   
}

</style>
