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
                {
                    label: "Shop",
                    link: "#",
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
    <header>
        <div class="left-side">
            <img :src=getImage(logo) alt="Logo">
        </div>
        <div class="right-side">
            <ul>
                <li v-for="link in headerLinks" :key="link.label">
                    <a :href="link.link"></a> {{ link.label }}
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
    padding: 2rem 4rem;
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
        color: rgb(36, 36, 36);

        a {
            text-decoration: none;
        }
    }
}
</style>
