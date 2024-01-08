<script>
import SingleCharacter from './SingleCharacter.vue'

    export default {
        name: 'CharactersList',
        components: {
            SingleCharacter
        }
    }
</script>

<template>
    <section class="container">
        <div class="row">
            <div class="col-3">
                <SingleCharacter />
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    
</style>
