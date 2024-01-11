<script>
import { store } from '../store.js'

export default {
    name: 'AppMain',
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
                <div class="col-20" v-for="card,index in store.cardsList" :key="index">
                    <div class="cards_container">
                    <img :src="card.card_images[0].image_url" :alt="card.name">
                    <h5 class="text-center my-3">{{card.name}}</h5>
                    <div class="text-center archetype">{{card.archetype}}</div>
                    </div>
                </div>
            </div>
        </div>
  </main>
</template>
<style lang="scss">
@use '../styles/partials/variables' as*;

main {
    background-color: $orange;
}

.bg-white {
    background-color: $white;
}

.col-20 {
    width: calc(100%/5 - 20px);
    margin: 10px;

    .cards_container {
        background-color: $orange;
        width: 100%;
        margin-bottom: 15px;
        height: calc(100% - 15px);

        img {
            max-width: 100%;
        }

        h5 {
            color: $white;
            text-transform: uppercase;
            font-weight: 600;
            text-align: center;
            margin: 1rem 0;
        }

        .archetype {
            font-size: 20px;
            text-align: center;
        }

    }
}
</style>