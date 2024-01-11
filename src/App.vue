<script>
import axios from 'axios'
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import { store } from './store.js'
export default {
  components: {
    AppHeader,
    AppMain
  },
  data() {
    return {
      store
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
  <div>
    <AppHeader />
    <AppMain />
  </div>
</template>
<style lang="scss">
@use './styles/generals.scss';
</style>