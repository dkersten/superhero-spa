<template>
    <main>

        <h1>Superheros</h1>
        <SuperHeroContainer />
    </main>
</template>

<script>
import SuperHeroContainer from './SuperheroContainer.vue'

export default {
  name: 'MainContainer',
  components: {
      SuperHeroContainer
  }
}
</script>

<style lang="css" scoped>
    @import url('https://fonts.googleapis.com/css2?family=Noto+Sans:wght@400;700&display=swap');

    * {
        font-family: 'Noto Sans', sans-serif;
    }

    main {
        width: 100%;
        max-width: 1240px;
        margin: 2rem auto;
        padding: 0 1rem;
    }

    h1 {
        font-size: 2.5rem;
        font-weight: 700;
        color: #1d1d1f;
        margin-bottom: 2.5rem;
    }
</style>