<!-- import axios from "axios"; -->
<script>
export default {
    name: "AppCards",

    props: {
        card: Object
    }
}
</script>

<template>
    <div class="ms_card text-center p-3">
        <img :src="card.card_images[0].image_url_small" alt="">
        <h5 class="ms_title text-white text-uppercase py-3">{{ card.name }}</h5>
        <div class="ms_archetype">{{ card.archetype }}</div>
    </div>
</template>

<style scoped lang="scss">
@use "../style/general" as *;
@use "../style/variables" as *;

.ms_card {
    background-color: $main-background-color;
    height: 100%;
}
</style>