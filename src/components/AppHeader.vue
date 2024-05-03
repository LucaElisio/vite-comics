<script>
    export default {
        data() {
            return {
                menu: [
                    {
                        title: "CHARACTERS",
                        isActive: false
                    },
                    {
                        title: "COMICS",
                        isActive: false
                    },
                    {
                        title: "MOVIES",
                        isActive: false
                    },
                    {
                        title: "TV",
                        isActive: false
                    },
                    {
                        title: "GAMES",
                        isActive: false
                    },
                    {
                        title: "COLLECTIBLES",
                        isActive: false
                    },
                    {
                        title: "VIDEOS",
                        isActive: true
                    },
                    {
                        title: "FANS",
                        isActive: false
                    },
                    {
                        title: "NEWS",
                        isActive: false
                    },
                    {
                        title: "SHOP",
                        isActive: false
                    }
                ]
            }
        }
    }
</script>

<template>
    <header>
        <div class="container">

            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="">
            </div>
            <div class="menu">
                <ul>
                    <li v-for="curLink in menu"><a href="" :class="{'active': curLink.isActive}">{{curLink.title}}</a></li>
                </ul>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
    @use "../style/partials/variables" as *;
    @use "../style/partials/mixins" as *;


    .container {
        @include flex(row, space-between, center)
    }

    header {

        height: 150px;
        @include flex(row, center, center);

        ul {
            @include flex (row, center, center);
            gap: 20px;

            li {
                list-style-type: none;

                a {
                    color: $secondary-color;
                    text-decoration: none;

                    &.active {
                        color: $primary-color;
                    }
                }

            }
        }
    }
</style>