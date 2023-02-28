<script>
export default {
    data() {
        return {
            logo: "dc-logo",
            dcComics: [
                {
                    label: "Characters",
                    link: "#",
                    active: false,
                },
                {
                    label: "Comics",
                    link: "#",
                    active: false,
                },
                {
                    label: "Movies",
                    link: "#",
                    active: false,
                },
                {
                    label: "Tv",
                    link: "#",
                    active: false,
                },
                {
                    label: "Games",
                    link: "#",
                    active: false,
                },
                {
                    label: "Collectible",
                    link: "#",
                    active: false,
                },
                {
                    label: "Videos",
                    link: "#",
                    active: false,
                },
                {
                    label: "Fans",
                    link: "#",
                    active: false,
                },
                {
                    label: "News",
                    link: "#",
                    active: false,
                },
            ],
            shopLinks: [
                {
                    label: "Shop DC",
                    link: "#",
                },
                {
                    label: "Shop DC Collectibles",
                    link: "#",
                },
            ],
            dcLinks: [
                {
                    label: "Term of Use",
                    link: "#",
                },
                {
                    label: "Privacy Policy (New)",
                    link: "#",
                },
                {
                    label: "Ad Choices",
                    link: "#",
                },
                {
                    label: "Advertising",
                    link: "#",
                },
                {
                    label: "Jobs",
                    link: "#",
                },
                {
                    label: "Subscriptions",
                    link: "#",
                },
                {
                    label: "Talent Workshops",
                    link: "#",
                },
                {
                    label: "CPSC Certificates",
                    link: "#",
                },
                {
                    label: "Ratings",
                    link: "#",
                },
                {
                    label: "Shop Help",
                    link: "#",
                },
                {
                    label: "Conact Us",
                    link: "#",
                },

            ],
            siteLinks: [
                {
                    label: "DC",
                    link: "#",
                },
                {
                    label: "MAD Magazine",
                    link: "#",
                },
                {
                    label: "DC Kids",
                    link: "#",
                },
                {
                    label: "DC Universe",
                    link: "#",
                },
                {
                    label: "DC Power Visa",
                    link: "#",
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
                            <a :href="link.link">{{ link.label }}</a>
                        </li>
                    </ul>
                    <ul>
                        <li>SHOP</li>
                        <li v-for="link in shopLinks">
                            <a :href="link.link">{{ link.label }}</a>
                        </li>
                    </ul>
                </div>
                <div class="right-side">
                    <ul>
                        <li>DC</li>
                        <li v-for="link in dcLinks">
                            <a :href="link.link">{{ link.label }}</a>
                        </li>
                    </ul>
                    <ul>
                        <li>SITES</li>
                        <li v-for="link in siteLinks">
                            <a :href="link.link">{{ link.label }}</a>
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
    background-size: 41%;
    background-repeat: no-repeat;
    bottom: 0;
    left: 11%;
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
    gap: 3rem;
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
