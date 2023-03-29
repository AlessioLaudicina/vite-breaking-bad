<script>
export default {
    name: 'Cards',
    props: {
        image: String,
        name: String,
        archetype: String,
    }
}


</script>


<template>
    <div class="card text-center">
        <img :src="image" class="img-fluid">
        <h3>{{ name }}</h3>
    </div>
</template>


<style scoped></style>