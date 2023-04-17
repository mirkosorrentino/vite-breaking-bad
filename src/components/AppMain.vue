<!-- import axios from "axios"; -->
<script>
import AppCards from './AppCards.vue'

export default {
    name: "AppMain",
    components: {
        AppCards
    },

}
</script>

<template>
    <main>
        <div class="ms_col" v-for="card in store.cards" :key="card.id">
            <AppCards :card="card"/>
        </div>
    </main>
</template>

<style scoped lang="scss">
@use "../style/general" as *;

// @use "../style/variables" as *;

</style>