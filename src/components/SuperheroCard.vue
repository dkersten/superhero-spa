<template>
    <div class="superhero-card">
        <img src="https://cdn.jsdelivr.net/gh/akabab/superhero-api@0.3.0/api/images/sm/1-a-bomb.jpg" />
        <h3>Hero Name</h3>
        <span>Full Name</span>
    </div>

</template>

<script>
export default {
    name: 'SuperheroCard',
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
    }

    h3 {
        font-weight: 700;
        color: #1d1d1f;
        font-size: 1.2rem;
        margin-bottom: 1rem;
    }
</style>