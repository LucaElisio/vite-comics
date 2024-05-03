<script>
export default {
    data(){
        return {
            footerLinks: [
                {
                    title: "dc comics",
                    links: ["Character", "Movies", "Comics", "TV", "Games", "Videos", "News"]
                },
                {
                    title: "shop",
                    links: ["Shop DC", "Shop DC Collectibles"]
                },
                {
                    title: "dc",
                    links: ["Character", "Movies", "Comics", "TV", "Games", "Videos", "News"]
                },
                {
                    title: "sites",
                    links: ["Character", "Movies", "Comics", "TV", "Games", "Videos", "News"]
                },
            ]
        }
    }
}
</script>

<template>
    <footer>
        <div class="container">
            <ul class="link-macrolist">
                <li v-for="curLinks in footerLinks">
                    <h4>{{curLinks.title}}</h4>
                    <ul class="link-list">
                        <li v-for="link in curLinks.links">
                            <a href="">{{link}}</a>
                        </li>
                    </ul>
                </li>
            </ul>
            <div class="bg-logo">
                <img src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>
        <div class="sign-up">

        </div>
    </footer>
</template>

<style lang="scss" scoped>
    @use "../style/partials/variables" as *;
    @use "../style/partials/mixins" as *;

    footer{
        background-image: url("../assets/img/footer-bg.jpg");
        background-position: center;
        background-size: cover;
        color: white;


        .container {
            @include flex($justify-content: space-between);
            position: relative;
            padding: 100px 0;
            
            .bg-logo{


                img {
                    position: absolute;
                    top: -100px;
                    right: 0;

                }
            }
        }
        // debug
        // height: 500px;

        .link-macrolist {
            list-style-type: none;
            @include flex($justify-content: flex-start, $gap: 20px, $align-items: flex-start);
            width: 50%;

            li {
                margin: 5px 0;
            }

            h4{
                text-transform: uppercase;
                margin: 10px 0;
            }

            a{
                color: gray;
                text-decoration: none;
            }

            .link-list {
                list-style-type: none;
            }

        }

        .sign-up{
            position: relative;
            z-index: 2;
            height: 100px;
            background-color: red;
        }

    }

</style>