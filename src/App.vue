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
    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=40@offset=0')
      .then(response => {
        this.store.elencoCards = response.data.data;
        console.log(this.store.elencoCards)
      })

  }
}
</script>

<template>
  <MyHeader></MyHeader>

  <main>
    <div class="container">
      <CardList></CardList>

    </div>



  </main>
</template>

<style lang="scss">
@use './styles/general.scss';
</style>
