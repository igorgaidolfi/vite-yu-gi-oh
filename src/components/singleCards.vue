<script>
export default {
    name: 'singleCards',
    props: {
        card: Object
    }
}
</script>
<template lang="">
<div class="col-20">
    <div class="cards_container">
    <img :src="card.card_images[0].image_url" :alt="card.name">
    <h5 class="text-center my-3">{{card.name}}</h5>
    <div class="text-center archetype">{{card.archetype}}</div>
    </div>
</div>
</template>
<style lang="scss">
@use '../styles/partials/variables' as*;

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
