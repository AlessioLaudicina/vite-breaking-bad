<script>
import { store } from '../store.js'
export default {
    name: 'ResultsMessage',
    data() {
        return {
            store
        }
    },
    computed: {
        message() {
            return `Sono state trovate ${this.store.elencoCards.length} carte`
        }
    }
}

</script>


<template>
    <div class="container">
        <h4> {{ message }}</h4>
    </div>
</template>

<style></style>