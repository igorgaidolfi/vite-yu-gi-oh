<script>
import axios from 'axios'
import { store } from '../store.js'
export default {
  name: 'CardList',
  data() {
    return {
      store,
      activeCard: 0
    }
  },
  methods: {
    getCardsList() {
      axios.get(store.endpoint).then((response) => {
        this.store.cardsList = response.data.data
      })
    },

  },
  created() {
    this.getCardsList()
  }
}
</script>
<template lang="">
  <div class="container">
    <div class="row">
        <div class="col-3" v-for="card,index in store.cardsList" :key="index">
          <img :src="store.cardsList[index].card_images[activeCard].image_url" :alt="store.cardsList[0].name">
          <h5>{{store.cardsList[index].name}}</h5>
          <div>{{store.cardsList[index].archetype}}</div>
            
        </div>
    </div>
 </div>
</template>
<style lang="">
  
</style>