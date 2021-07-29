<template>
    <div>

        <!-- Create child hero cards only when API data is loaded -->
        <div class="flex-container" v-if="heros !== null">

            <SuperheroCard class="blah" v-for="hero in heros" :key="hero.id" :parentData="hero" />
        </div>

        <!-- Notify user data is loading if connection speed is slow -->
        <div v-else>
            <p>Please wait while our heros download...</p>
        </div>

    </div>
</template>

<script>

// imports
import SuperheroCard from './SuperheroCard.vue'
import axios from 'axios'

export default {
    name: 'SuperHeroContainer',
    components: {
        SuperheroCard
    },

    data() {
        return {
            heros: null,
            testStuff: [1,2,3,4,5]
        }
    },

    mounted() {
        axios
            .get('https://akabab.github.io/superhero-api/api/all.json')
            .then(response => (this.heros = response.data))
    }
}
</script>

<style lang="css" scoped>
    .flex-container {
        display: flex;
        flex-wrap: wrap;
        align-items: stretch;
        justify-content: center;
    }
</style>