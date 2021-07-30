<template>
    <div class="superhero-card">

        <img v-bind:src="hero.images.sm" v-bind:alt="hero.name + ' ' + 'illustrative portrait' " />

        <h2>Name: {{hero.name}}</h2>

        <span v-if="hero.biography.fullName !== ''" class="full-name">

            <span class="bold">Full Name:</span> {{hero.biography.fullName}}
        </span>
        <span v-else>
            No full name
        </span>

        <!-- Toggle show more/less btn based on state -->
        <button v-if="showMore === true" v-on:click="toggleShowMore" v-bind:aria-label="'See less information about ' + hero.name">Show Less</button>

        <button v-else v-on:click="toggleShowMore" v-bind:aria-label="'See more information about ' + hero.name">
            See More
        </button>

        <div v-if="showMore" class="show-more">
            <h3>Stats</h3>
            <ul>
                <li>Intelligence: {{hero.powerstats.intelligence}}</li>
                <li>Strength: {{hero.powerstats.strength}}</li>
                <li>Speed: {{hero.powerstats.speed}}</li>
                <li>Durability: {{hero.powerstats.durability}}</li>
                <li>Power: {{hero.powerstats.power}}</li>
                <li>Combat: {{hero.powerstats.combat}}</li>
            </ul>
        </div>

    </div>
</template>

<script>

export default {
    name: 'SuperheroCard',
    props: {
        parentData: Object
    },

    data() {
        return {
            hero: this.parentData,
            showMore: false
        }
    },

    mounted() {
        // console.log(this.parentData)
    },
    methods: {
        toggleShowMore : function() {
            this.showMore = !this.showMore
            console.log(this.showMore)
        }
    }
    
}
</script>

<style lang="css" scoped>
    .superhero-card {
        background: #fbfbfd;
        margin: 1rem;
        padding: 1rem 1.5rem;
        box-shadow: rgba(17, 17, 26, 0.15) 0px 4px 16px, rgba(17, 17, 26, 0.15) 0px 8px 32px;
        border-radius: 8px;
        width: 225px;
    }

    img {
        display: block;
        margin: 0 auto 1.5rem;
        max-width: 100%;
    }

    h2 {
        font-weight: 700;
        color: #1d1d1f;
        font-size: 1.2rem;
        margin-bottom: 1rem;
    }

    .full-name {
        line-height: 1.5;
    }

    .bold {
        font-weight: 700;
    }

    button {
        display: block;
        margin: 1.5rem auto 0;
        padding: 14px 40px;
        border: none;
        border-radius: 20px;
        background: linear-gradient(to right, #1CB5E0 0%, #000851 100%);
        color: #fff;
        text-shadow: 1px 1px 3px rgba(0,0,0,.5);
        font-weight: 700;
    }

    button:hover {
        background: linear-gradient(to left, #1CB5E0 0%, #000851 100%);
        cursor: pointer;
    }

    .show-more {
        margin-top: 1.5rem;
    }

    h3 {
        font-weight: 700;
        margin-bottom: .5rem;
    }

    li {
        line-height: 1.4;
        list-style: disc;
        margin-left: 1.25rem;
    }

</style>