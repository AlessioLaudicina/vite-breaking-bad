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
        <img :src="image">
        <h4>{{ name }}</h4>
        <h5>{{ archetype }}</h5>
    </div>
</template>


<style scoped>
.card {
    text-align: center;
    height: 300px;
    margin: 10px;
    background-color: rgb(197, 135, 20);
    ;
    border-radius: 0;
    padding-bottom: 20px;
    position: relative;
}

img {
    padding: 10px;
    height: 180px;

}

h5 {

    font-size: 0.7rem;
    font-weight: 700;
    margin-bottom: 20px;
    padding-top: 10px
}

p {

    font-size: 0.8rem;
    margin: 0;
}
</style>