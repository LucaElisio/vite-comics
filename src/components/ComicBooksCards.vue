<script>
export default {
    props: {
                cardThumb: String,
                cardSeries: String,
            },

    data() {
        return {


        }
    },
}
</script>

<template>
    <div class="card">
        <img :src="cardThumb" :alt="CardSeries" />
        <h5>{{cardSeries}}</h5>
    </div>
</template>

<style scoped lang="scss">
    
    img {
        width: 100%;
        aspect-ratio: 1;
        object-fit: cover;
        object-position: top;
        margin-bottom: 1rem;
    }

    h5 {
        text-transform: uppercase;
    }


</style>