<script>
    export default {
        data() {
            return {

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
                    <li><a href="" class="active">CHARACTERS</a></li>
                    <li><a href="">COMICS</a></li>
                    <li><a href="">MOVIES</a></li>
                    <li><a href="">TV</a></li>
                    <li><a href="">GAMES</a></li>
                    <li><a href="">COLLECTIBLES</a></li>
                    <li><a href="">VIDEOS</a></li>
                    <li><a href="">FANS</a></li>
                    <li><a href="">NEWS</a></li>
                    <li><a href="">SHOP</a></li>
                </ul>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
    @use "../style/partials/variables" as *;
    @use "../style/partials/mixins" as *;

    .container {
        width: 80%;
        margin: 0 auto;
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