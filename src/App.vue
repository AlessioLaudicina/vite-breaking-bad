<script>
import axios from 'axios';
import { store } from './store.js';
import MyHeader from './components/MyHeader.vue';
import AppSearch from './components/AppSearch.vue';
import ResultsMessage from './components/ResultsMessage.vue';
import CardList from './components/CardList.vue';
export default {
  components: {
    MyHeader,
    AppSearch,
    ResultsMessage,
    CardList,
  },
  data() {
    return {
      store

    }
  },
  methods: {
    getCards() {
      console.log(store.search);

      let urlApi = 'https://db.ygoprodeck.com/api/v7/cardinfo.php?num=40&offset=0';

      if (store.search != '') {
        urlApi += `&archetype=${store.search}`
      }

      axios.get(urlApi)
        .then(response => {
          this.store.elencoCards = response.data.data;
          console.log(this.store.elencoCards)
        })

    }

  },
  created() {
    this.getCards();

  }
}
</script>

<template>
  <MyHeader></MyHeader>

  <main>
    <div class="container">
      <AppSearch @doSearch="getCards"></AppSearch>
      <ResultsMessage></ResultsMessage>
      <CardList></CardList>

    </div>



  </main>
</template>

<style lang="scss">
@use './styles/general.scss';
</style>
