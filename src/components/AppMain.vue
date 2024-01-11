<script>
import singleCards from './singleCards.vue';
import { store } from '../store.js'

export default {
    name: 'AppMain',
    components: {
        singleCards,
    },
    data() {
        return {
            store,
        }
    }
}
</script>
<template lang="">
  <main>
        <div class="container">
            <select class="form-select mb-4">
                <option selected>Alien</option>
            </select>
        </div>
        <div class="container bg-white">
            <div class="row">
                <singleCards v-for="card,index in store.cardsList" :key="index" :card="card"/>
            </div>
        </div>
  </main>
</template>
<style lang="scss">
@use '../styles/partials/variables' as*;

.bg-white {
    background-color: $white;
}
</style>