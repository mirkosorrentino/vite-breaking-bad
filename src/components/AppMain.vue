<!-- import axios from "axios"; -->
<script>
import AppCards from './AppCards.vue'
import { store } from '../store'
export default {
    name: "AppMain",
    components: {
        AppCards
    },
    data() {
        return {
            store
        }
    }

}
</script>

<template>
    <main>
        <div class="grid">
            <div class="row">
                <div class="col-3 py-3" v-for="card in store.cards" :key="card.id">
                    <AppCards :card="card"/>
                </div>
            </div>
        </div>
    </main>
</template>

<style scoped lang="scss">
@use "../style/general" as *;
@use "../style/mixins" as *;

// @use "../style/variables" as *;
</style>