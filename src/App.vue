<script>
import axios from "axios";
import { store } from "./store";

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

export default {
  components: {
    AppHeader,
    AppMain
  },

  data(){
    return {
      store
    }
  },

  mounted() {
    axios.get("store.apiURL").then((resp) => {
      this.store.cards = resp.data.data;
      console.log(resp);
    })
  }
}
</script>

<template>
  <AppHeader/>
  <AppMain/>
</template>

<style lang="scss">
@use "./style/general.scss";
</style>
