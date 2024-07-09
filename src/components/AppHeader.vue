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

            ],
            activeIndex: null,
        }
    },
    methods: {
        setActive(index) {
            this.activeIndex = index;
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
                    <li v-for="(link, index) in links" :key="index" :class="{ active: index === activeIndex }"
                    @click="setActive(index)">
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

                .active {
                    color: #0282f9;
                    border-bottom: 4px solid #0282f9;
                }

                li {
                    height: 100px;
                    line-height: 100px;
                    vertical-align: middle;
                }

                li:hover {
                    color: #0282f9;
                    border-bottom: 4px solid #0282f9;
                }
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