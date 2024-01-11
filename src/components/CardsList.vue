<script>

import { store } from '../store.js'
export default {
  name: 'CardList',
  data() {
    return {
      store,
    }
  }
}
</script>
<template lang="">
  <div class="container bg_white">
    <div class="container">
      <div class="row">
          <div class="col_20" v-for="card,index in store.cardsList" :key="index">
            <div class="cards_container">
              <img :src="card.card_images[0].image_url" class="img-fluid" :alt="card.name">
              <h5 class="text-center my-3">{{card.name}}</h5>
              <div class="text-center archetype">{{card.archetype}}</div>
            </div>
          </div>
      </div>
   </div>
  </div>
</template>
<style lang="scss">
@use '../styles/partials/variables' as*;

.bg_white {
  background-color: $white_;
  padding: 50px 0;
}

.row .col_20 {
  width: calc(100%/5);
}

.cards_container {
  background-color: $orange_;
  margin-bottom: 15px;
  height: calc(100% - 15px);

  h5 {
    color: $white_;
    text-transform: uppercase;
    font-weight: 600;
  }

  .archetype {
    font-size: 20px;
  }
}
</style>