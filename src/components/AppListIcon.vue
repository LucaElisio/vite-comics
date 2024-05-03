<script>


export default {
    data(){
        return {
            images: [
                {
                    logo: "buy-comics-digital-comics.png",
                    title: "digital comics"
                },
                {
                    logo: "buy-comics-merchandise.png",
                    title: "dc merchandise"
                },
                {
                    logo: "buy-comics-subscriptions.png",
                    title: "subscription"
                },
                {
                    logo: "buy-comics-shop-locator.png",
                    title: "comic shop locator"
                },
                {
                    logo: "buy-dc-power-visa.svg",
                    title: "dc power visa"
                }
            ]
        }
    },
    methods: {
        getImageUrl(imageName){
            return new URL(`../assets/img/${imageName}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <section class="icon-list">
        <div class="container">
            <ul>
                <li v-for="curImg in images">
                    <img :src="getImageUrl(curImg.logo)" alt="">
                    <a href="">{{curImg.title}}</a>
                </li>
            </ul>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    @use "../style/partials/variables" as *;
    @use "../style/partials/mixins" as *;
    @use "../style/partials/layout" as *;

.icon-list {
    width: 100%;
    background-color: $primary-color;
    position: relative;
    z-index: 2;
}

.container{
    padding: 50px 0;
}

ul {
    @include flex($justify-content: space-evenly);

    li {
        @include flex($gap: 10px);

        a {
            color: white;
            font-size: 1rem;
            text-transform: uppercase;
            text-decoration: none;

        }
    }
}

img {
    height: 5rem;
}

</style>