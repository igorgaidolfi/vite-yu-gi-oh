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
    <div class="bg-list-cards p-4">
        <div class="container">
            <div class="col-1">
                <select class="form-select mb-4">
                    <option selected>Alien</option>
                </select>
            </div>
        </div>
        <CardsList/>
    </div>
  </main>
</template>
<style lang="scss">
@use '../styles/partials/variables' as*;

main {
    background-color: $orange_;
}
</style>