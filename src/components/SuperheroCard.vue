<template>
    <div class="superhero-card">

        <img v-bind:src="heroPic" v-bind:alt="hero.name + ' ' + 'illustrative portrait' " />

        <h2>Name: {{hero.name}}</h2>

        <span v-if="hero.biography.fullName !== ''" class="full-name">

            <span class="bold">Full Name:</span> {{hero.biography.fullName}}
        </span>
        <span v-else>
            No full name
        </span>

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
            heroPic: this.parentData.images.sm
        }
    },

    mounted() {
        // console.log(this.parentData)
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
</style>