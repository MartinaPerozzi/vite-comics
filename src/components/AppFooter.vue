<script>
export default {
    data() {
        return {
            logo: "dc-logo",
            dcComics: [
                {
                    label: "Characters",
                    url: "#",
                    active: false,
                },
                {
                    label: "Comics",
                    url: "#",
                    active: false,
                },
                {
                    label: "Movies",
                    url: "#",
                    active: false,
                },
                {
                    label: "Tv",
                    url: "#",
                    active: false,
                },
                {
                    label: "Games",
                    url: "#",
                    active: false,
                },
                {
                    label: "Collectible",
                    url: "#",
                    active: false,
                },
                {
                    label: "Videos",
                    url: "#",
                    active: false,
                },
                {
                    label: "Fans",
                    url: "#",
                    active: false,
                },
                {
                    label: "News",
                    url: "#",
                    active: false,
                },
            ],
            shopLinks: [
                {
                    label: "Shop DC",
                    url: "#",
                },
                {
                    label: "Shop DC Collectibles",
                    url: "#",
                },
            ],
            dcLinks: [
                {
                    label: "Term of Use",
                    url: "#",
                },
                {
                    label: "Privacy Policy (New)",
                    url: "#",
                },
                {
                    label: "Ad Choices",
                    url: "#",
                },
                {
                    label: "Advertising",
                    url: "#",
                },
                {
                    label: "Jobs",
                    url: "#",
                },
                {
                    label: "Subscriptions",
                    url: "#",
                },
                {
                    label: "Talent Workshops",
                    url: "#",
                },
                {
                    label: "CPSC Certificates",
                    url: "#",
                },
                {
                    label: "Ratings",
                    url: "#",
                },
                {
                    label: "Shop Help",
                    url: "#",
                },
                {
                    label: "Conact Us",
                    url: "#",
                },

            ],
            siteLinks: [
                {
                    label: "DC",
                    url: "#",
                },
                {
                    label: "MAD Magazine",
                    url: "#",
                },
                {
                    label: "DC Kids",
                    url: "#",
                },
                {
                    label: "DC Universe",
                    url: "#",
                },
                {
                    label: "DC Power Visa",
                    url: "#",
                },
            ],

        };

    },

    methods: {
        getImage(name) {
            return new URL(`../assets/img/${name}`, import.meta.url).href;
        }
    },
}

</script>

<template>
    <footer>
        <div class="links-container">
            <div class="container">
                <div class="left-side">
                    <ul>
                        <li>DC COMICS</li>
                        <li v-for="link in dcComics">
                            <a :href="link.url">{{ link.label }}</a>
                        </li>
                    </ul>
                    <ul>
                        <li>SHOP</li>
                        <li v-for="link in shopLinks">
                            <a :href="link.url">{{ link.label }}</a>
                        </li>
                    </ul>
                </div>
                <div class="right-side">
                    <ul>
                        <li>DC</li>
                        <li v-for="link in dcLinks">
                            <a :href="link.url">{{ link.label }}</a>
                        </li>
                    </ul>
                    <ul>
                        <li>SITES</li>
                        <li v-for="link in siteLinks">
                            <a :href="link.url">{{ link.label }}</a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang= "scss" scoped>
.links-container {
    display: flex;
    gap: 2rem;
    background-image: url(../assets/img/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    padding: 5rem 5rem;
    position: relative;

    .container {
        display: flex;
        gap: 2rem;
        width: 100%;

    }
}

.links-container:before {
    content: "";
    background-image: url(../assets/img/dc-logo-bg.png);
    position: absolute;
    background-size: 40%;
    background-repeat: no-repeat;
    bottom: 0;
    left: 20%;
    width: 100%;
    height: 100%;
    background-position: center;

}

.right-side {
    display: flex;
    justify-content: center;
    align-content: center;
    gap: 2.5rem;
}

.left-side {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-content: center;
    gap: 2rem;
}

ul {
    list-style-type: none;

    li {
        color: white;

        a {
            color: white;
            text-decoration: none;
        }
    }
}

li:first-child {
    font-size: 1.5rem;
    padding-bottom: 1rem;
}
</style>
