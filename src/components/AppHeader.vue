<script>
export default {
    name: "AppHeader",

    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                },
                {
                    text: "COMICS",
                    url: "#",
                },
                {
                    text: "MOVIES",
                    url: "#",
                },
                {
                    text: "TV",
                    url: "#",
                },
                {
                    text: "GAMES",
                    url: "#",
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                },
                {
                    text: "VIDEOS",
                    url: "#",
                },
                {
                    text: "FANS",
                    url: "#",
                },
                {
                    text: "NEWS",
                    url: "#",
                },
                {
                    text: "SHOP",
                    url: "#",
                },

            ]
        }
    }
}
</script>

<template>
    <header>
        <div class="container">
            <a href="#" class="logo">
                <img src="../assets/dc-logo.png" alt="Logo">
            </a>

            <nav>
                <ul>
                    <li v-for="(link, index) in links" :key="index">
                        <a :href="link.url">
                            {{ link.text }}
                        </a>
                    </li>
                </ul>
            </nav>

        </div>
        <div class="jumbotron">
            <div class="container">
                <a href="#" class="button">
                    CURRENT SERIES
                </a>
            </div>
        </div>
    </header>

</template>

<style lang="scss" scoped>

    header{

        .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 100px;

            .logo {
            width: 50px;
            aspect-ratio: 1/1;
            }

            ul {
                display: flex;
                gap: 20px;
                align-items: center;
                font-size: small;
            }

        }

        .jumbotron {
            background-image: url("../assets/jumbotron.jpg");
            height: 350px;
            background-size: cover;
            position: relative;

            .button {
                padding: 10px 25px;
                background-color: #0282f9;
                color: #fff;
                font-weight: bold;
                position: absolute;
                bottom: -20px;
                left: 150px;
            }
        }

    }


    
</style>