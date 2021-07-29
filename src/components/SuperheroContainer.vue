<template>
    <div class="flex-container">
        <SuperheroCard />
        <SuperheroCard />
        <SuperheroCard />
        <SuperheroCard />
        <SuperheroCard />
        <SuperheroCard />
        <SuperheroCard />
    </div>
</template>

<script>

import SuperheroCard from './SuperheroCard.vue'

export default {
    name: 'SuperHeroContainer',
    components: {
        SuperheroCard
    }
}
</script>

<style lang="css" scoped>
    .flex-container {
        border: 1px solid #cecece;
        display: flex;
        flex-wrap: wrap;
        align-items: flex-start;
        justify-content: center;
    }
</style>