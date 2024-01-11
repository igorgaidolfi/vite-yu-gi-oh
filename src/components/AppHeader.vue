<script>
export default {
    name: 'AppHeader'
}
</script>
<template lang="">
    <header>
        <div class="container">
            <div class="row">
                <h1>Yu-Gi-Oh Api</h1>
            </div>
        </div>
    </header>
</template>
<style lang="scss">
@use '../styles/partials/variables' as*;

header {
    background-color: $white;
    padding: 20px 0;
}
</style>