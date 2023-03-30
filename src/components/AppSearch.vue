<script>
import { store } from '../store.js'
export default {
    name: 'AppSearch',
    data() {
        return {
            store
        }
    }

}
</script>

<template>
    <div class="my-container">
        <select @change="$emit('doSearch')" v-model="store.search">
            <option value="">Select archetype</option>
            <option value="alien">Alien</option>
            <option value="A.I.">A.I.</option>
            <option value="Unchained">Unchained</option>
            <option value="Dragunity">Dragunity</option>

        </select>

    </div>
</template>

<style scoped>
.my-container {
    width: 70%;
    margin: 0 auto;
}

select {
    width: 200px;
    margin-bottom: 20px;
}
</style>