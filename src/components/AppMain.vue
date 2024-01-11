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
            archtypes: [
                'Alien',
                'Infernoble Arms',
                'Noble Knight',
                'Melodious',
                'Archfiend'
            ]
        }
    },
    methods: {
        selectType() {
            return this.store.type
        }
    },
}
</script>
<template lang="">
  <main>
        <div class="container">
            <select v-model="store.type" @change="$emit('select_type')">
                <option value="" selected>Select</option>
                <option v-for="type,index in archtypes" :key="index" :value="type">{{ type }}</option>
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

select {
    width: 15%;
    height: 30px;
    margin: 20px 0px 20px 10px;
    padding-left: 10px;
    font-size: medium;
}
</style>