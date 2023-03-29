<script>
import { store } from '../store.js';
import Cards from './Cards.vue';
export default {
    name: 'CardList',
    data() {
        return {
            store
        }
    },
    components: {
        Cards,
    }
}

</script>


<template>
    <div class="container">
        <div class="row">
            <div class="col-3" v-for=" ( card, index) in store.elencoCards" :key="index">
                <Cards :image="card.image_url" :name="card.name" :archetype="card.archetype"></Cards>


            </div>

        </div>
    </div>
</template>


<style scoped></style>