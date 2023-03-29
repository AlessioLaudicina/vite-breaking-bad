<script>
import axios from 'axios';
import { store } from './store.js';
import MyHeader from './components/MyHeader.vue';
import CardList from './components/CardList.vue';
export default {
  components: {
    MyHeader,
    CardList,
  },
  data() {
    return {
      store

    }
  },
  created() {
    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
      .then(response => {
        this.store.elencoCards = response.data;
      })

  }
}
</script>

<template>
  <MyHeader></MyHeader>

  <main>

    <CardList></CardList>

  </main>
</template>

<style lang="scss">
@use './styles/general.scss';
</style>
