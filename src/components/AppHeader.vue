<script>
export default {
    data() {
        return {
            logo: "dc-logo",
            headerLinks: [
                {
                    label: "Characters",
                    link: "#",
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
                {
                    label: "Shop",
                    url: "#",
                    active: false,
                },
            ]
        };
    },

    methods: {
        getImage(name) {
            return new URL(`../assets/img/${name}.png`, import.meta.url).href;
        }
    },
}

</script>

<template>
    <header class="container">
        <div class="left-side">
            <img :src=getImage(logo) alt="Logo">
        </div>
        <div class="right-side">
            <ul>
                <li v-for="link in headerLinks" :key="link.label">
                    <a :href="link.url"> {{ link.label }}</a>
                </li>
            </ul>
        </div>

    </header>
</template>

<style lang="scss" scoped>
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 0rem;

    img {
        width: 70%;
        min-width: 50px;
    }
}

ul {
    list-style-type: none;
    display: flex;
    flex-direction: row;
    gap: 2rem;

    li {
        text-transform: uppercase;
        font-family: 'Titillium Web', sans-serif;
        font-weight: 600;

        a {
            text-decoration: none;
            color: rgb(36, 36, 36);
        }
    }
}
</style>
