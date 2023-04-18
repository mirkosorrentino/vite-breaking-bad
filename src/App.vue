<script>
import axios from "axios";
import { store } from "./store";

import AppHeader from './components/AppHeader.vue';
import SelectionList from './components/SelectionList.vue';
import AppMain from './components/AppMain.vue';

export default {
  components: {
    AppHeader,
    SelectionList,
    AppMain,
  },

  data(){
    return {
      store
    }
  },

  mounted() {
    // axios.get(store.apiURL).then((resp) => {
    //   this.store.cards = resp.data.data;
    // })
    this.getCards()
  },

  methods: {
    getCards() {
      const params = {};
      if (this.store.selectedStatus) {
        params.status = this.store.selectedStatus;
      axios.get(this.store.apiURL, {
      params
      }).then(resp => {
        this.store.cards = resp.data.data;
      })
      }
    }, 

    handleSearch() {
      this.getCards()
    }
  }
    
}
</script>

<template>
  <AppHeader/>
  <SelectionList @search="handleSearch"/>
  <AppMain/>
</template>

<style lang="scss">
@use "./style/general.scss";
</style>
