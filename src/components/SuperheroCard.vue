<template v-if="superheroData.length > 0" >
    <div class="superhero-card">
        <img v-bind:src="heroPic" v-bind:alt="hero.name + ' ' + 'illustrative portrait' " />
        <h3>Name: {{hero.name}}</h3>
        <span v-if="hero.biography.fullName !== ''" class="full-name">

            <span class="bold">Full Name:</span> {{hero.biography.fullName}}
        </span>
        <!-- <span> {{ stuff }} </span> -->
    </div>

</template>

<script>

export default {
    name: 'SuperheroCard',
    props: {
        // mytest: 'testinggg',
        parentData: Object
    },

    data() {
        console.log(this.parentData) 
        return {
            hero: this.parentData,
            heroPic: this.parentData.images.sm
        }
    },

    mounted() {
        console.log(this.parentData)
    }
    
}
</script>

<style lang="css" scoped>
    .superhero-card {
        background: #fbfbfd;
        margin: 1rem;
        padding: 1rem 1.5rem;
        box-shadow: rgba(50, 50, 93, 0.25) 0px 13px 27px -5px, rgba(0, 0, 0, 0.3) 0px 8px 16px -8px;
        border-radius: 8px;
        width: 225px;
    }

    img {
        display: block;
        margin: 0 auto 1.5rem;
        max-width: 100%;
    }

    h3 {
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