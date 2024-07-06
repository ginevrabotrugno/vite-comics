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
            ]
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

                </div>
           </section>
 
    </footer>
</template>

<style lang="scss" scoped>
.links {
  background-image: url("../assets/footer-bg.jpg");
  background-size: cover;
  padding: 20px 0;

  .container {
    display: flex;
    justify-content: flex-start;
    gap: 30px;
    padding: 0 15px;

    h3 {
    color: #fff;
    font-size: 20px;
    margin-bottom: 10px;
    }

    ul {
    list-style: none;
    padding: 0;

        li {
            margin-bottom: 5px;

                a {
                color: #676767;
                font-size: 15px;
                text-decoration: none;

                &:hover {
                    color: #fff;
                }
                }
            }
        }
    }   
}


</style>