<script>
import AppCardsList from './AppCardsList.vue';
export default {
    name: 'AppMain',
    components: {
        AppCardsList,
    }

}
</script>
<template lang="">
  <main>
    <div class="bg-list-cards p-5">
        <AppCardsList/>
    </div>
  </main>
</template>
<style lang="scss">
@use '../styles/partials/variables' as*;

main {
    background-color: $orange_;
}
</style>