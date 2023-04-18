<script>
import { store } from '../store';

export default {
    name: "SelectionList",
    emits: ["search"],
    data() {
        return {
            store,
            archetypeChoices: ["None", "Alien", "Ally Of Justice", "Ancient Gear"]
        }
    }
}
</script>

<template>
    <div class="ms_container">
        <div class="ms_selector mb-3">
            <span class="px-2">Choose a filter:</span>
            <select name="chooseType" id="chooseType" v-model="store.selectedStatus">
                <option :value="archetype" v-for="archetype in archetypeChoices">{{ archetype }}</option>
            </select>
            <button @click="$emit('search')" class="btn btn-warning mx-2">Search</button>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../style/variables" as *;

</style>