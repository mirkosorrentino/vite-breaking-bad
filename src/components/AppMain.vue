<!-- import axios from "axios"; -->
<script>
import AppCards from './AppCards.vue'
import { store } from '../store'
export default {
    name: "AppMain",
    components: {
        AppCards,
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
        <div class="ms_container">
            <div class="grid ms_grid">
                <div class="row">
                    <div class="col-3 py-3" v-for="card in store.cards" :key="card.id">
                        <AppCards :card="card"/>
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>

<style scoped lang="scss">
@use "../style/mixins" as *;
@use "../style/variables" as *;

main {
    background-color: $main-background-color;
.ms_grid {
    background-color: white;
    padding: 10px 30px;
}
}
</style>