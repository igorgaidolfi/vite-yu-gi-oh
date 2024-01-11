<script>
import CardsList from './CardsList.vue';
export default {
    name: 'AppMain',
    components: {
        CardsList,
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
        <CardsList/>
  </main>
</template>
<style lang="scss">
@use '../styles/partials/variables' as*;

main {
    background-color: $orange;
}
</style>