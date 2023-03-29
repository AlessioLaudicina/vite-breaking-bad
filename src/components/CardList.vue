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
            <Cards></Cards>

        </div>
    </div>
</template>


<style scoped></style>