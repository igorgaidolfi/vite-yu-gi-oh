<script>
export default {
    name: 'singleCards',
    props: {
        card: Object
    }
}
</script>
<template lang="">
<div class="col-3">
    <img :src="card.cardsList[0].card_images[0].image_url" :alt="card.cardsList[0].name">
    <h5>{{card.cardsList[0].name}}</h5>
    <div>{{card.cardsList[0].archetype}}</div>
</div>
</template>
<style lang="">
    
</style>