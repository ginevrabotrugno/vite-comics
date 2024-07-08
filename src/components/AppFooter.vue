<script>
export default {
    name: "AppFooter",

    data () {
        return {
            lists: [
                {
                    title: "DC COMICS",
                    links: [
                        {
                            name: "Characters",
                            url: "#"
                        },
                        {
                            name: "Comics",
                            url: "#"
                        },
                        {
                            name: "Movies",
                            url: "#"
                        },
                        {
                            name: "TV",
                            url: "#"
                        },
                        {
                            name: "Games",
                            url: "#"
                        },
                        {
                            name: "Videos",
                            url: "#"
                        },
                        {
                            name: "News",
                            url: "#"
                        },
                    ]
                },
                {
                    title: "SHOP",
                    links: [
                        {
                            name: "Shop DC",
                            url: "#"
                        },
                        {
                            name: "Shop DC Collectibles",
                            url: "#"
                        },
                        
                    ]
                },
                {
                    title: "DC",
                    links: [
                        {
                            name: "Terms of Use",
                            url: "#"
                        },
                        {
                            name: "Privacy policy(New)",
                            url: "#"
                        },
                        {
                            name: "Ad Choices",
                            url: "#"
                        },
                        {
                            name: "Advertizing",
                            url: "#"
                        },
                        {
                            name: "Jobs",
                            url: "#"
                        },
                        {
                            name: "Subscriptions",
                            url: "#"
                        },
                        {
                            name: "Talent Workshops",
                            url: "#"
                        },
                        {
                            name: "CPSC Certificates",
                            url: "#"
                        },
                        {
                            name: "Ratings",
                            url: "#"
                        },
                        {
                            name: "Shop Help",
                            url: "#"
                        },
                        {
                            name: "Contact Us",
                            url: "#"
                        },
                    ]
                },
                {
                    title: "SITES",
                    links: [
                        {
                            name: "DC",
                            url: "#"
                        },
                        {
                            name: "MAD Magazine",
                            url: "#"
                        },
                        {
                            name: "DC Kids",
                            url: "#"
                        },
                        {
                            name: "DC Universe",
                            url: "#"
                        },
                        {
                            name: "DC Power Visa",
                            url: "#"
                        },
                    ]
                },
            ],
            icons: [
            {
                    src: "footer-facebook.png",
                    url: "#"
                },
                {
                    src: "footer-periscope.png",
                    url: "#"
                },
                {
                    src: "footer-pinterest.png",
                    url: "#"
                },
                {
                    src: "footer-twitter.png",
                    url: "#"
                },
                {
                    src: "footer-youtube.png",
                    url: "#"
                },
                
            ]
        }
    },
    methods: {
        getImagePath(imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
}
</script>

<template>
    <footer>
           <section class="links">
                <div class="container">

                    <ul v-for="(list, index) in lists" :key="index">
                        <li>
                            <h3>
                                {{ list.title }}
                            </h3>
                            <ul>
                                <li v-for="(link, index) in list.links" :key="index">
                                    <a :href="link.url">{{ link.name }}</a>
                                </li>
                            </ul>
                        </li>
                    </ul>

                </div>
           </section>
           <section class="sign-up">
                <div class="container">

                    <a href="#" class="button">
                        SIGN-UP NOW!
                    </a>

                    <nav>
                        <ul>
                            <li class="follow">FOLLOW US</li>
                            <li v-for="(icon, index) in icons" :key="index">
                                <a :href="icon.url">
                                    <img :src="getImagePath(`../assets/${icon.src}`)" alt="logo">
                                </a>
                            </li>
                        </ul>
                    </nav>
                </div>
            </section>
 
    </footer>
</template>

<style lang="scss" scoped>
.links {
    background-image: url("../assets/footer-bg.jpg");
    background-size: cover;
    padding: 20px 0;
    overflow: hidden;

    .container {
        max-height: 400px;
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;
        align-items: flex-start;
        align-content: flex-start;
        gap: 30px;
        padding: 15px 0;
        position: relative;

        &::after {
            content: url("/src/assets/dc-logo-bg.png");
            object-fit: cover;
            position: absolute;
            top: -81px;
            right: 0;
            width: 500px;
            aspect-ratio: 1/1;
        }

        h3 {
            color: #fff;
            font-size: 15px;
            margin-bottom: 10px;
        }

        ul {
            list-style: none;

                li {
                    margin-bottom: 5px;

                        a {
                        color: #676767;
                        font-size: smaller;
                        text-decoration: none;

                            &:hover {
                                color: #fff;
                            }
                        }
                    }
        }
    }   
}

.sign-up {
    background-color: #303030;
    color: #fff;
    height: 80px;

    .container {
        height: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;

        .button {
            padding: 10px 25px;
            border: solid 4px #0874d9;
            font-weight: bold;
        }

        ul {
            display: flex;
            gap: 20px;
            align-items: center;

            .follow {
                font-weight: bold;
                color: #0874d9;
            }
        }
    }
}


</style>