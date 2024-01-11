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
      let apiUrl = store.endpoint
      if (store.type != '') {
        apiUrl += `&archetype=${store.type}`
      }
      console.log(apiUrl)
      axios.get(apiUrl).then((response) => {
        store.cardsList = response.data.data
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
    <AppMain @select_type="getCardsList"/>
  </div>
</template>
<style lang="scss">
@use './styles/generals.scss';
</style>