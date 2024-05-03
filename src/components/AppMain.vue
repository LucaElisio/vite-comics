<script>
export default {
    data(){
        return {

        }
    }
}
</script>

<template>
    <main>
        <div class="container">
            <p>--> COTENT GOES HERE<--</p>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;


main {
    width: 100%;
    background-color: $secondary-color;
    color: white;

    /* debug */
    padding: 50px;

    p {
        font-size: 2rem;
    }
}

</style>