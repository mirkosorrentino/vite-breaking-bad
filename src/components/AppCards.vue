<!-- import axios from "axios"; -->
<script>
export default {
    name: "AppCards",

    props: {
        cards: Object
    }
}
</script>

<template>
    <div class="ms_card">
        <img src="" alt="">
        <h5 class="ms_title text-center text-white text-uppercase">{{ cards.name }}</h5>
        <div class="ms_archetype"></div>
    </div>
</template>

<style scoped lang="scss">
@use "../style/general" as *;
@use "../style/variables" as *;

.ms_card {
    background-color: $main-background-color;
}
</style>