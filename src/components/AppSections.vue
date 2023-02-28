<script>
export default {
    data() {
        return {
            sections: [
                {
                    productImg: "buy-comics-digital-comics.png",
                    label: "Digital Comics",
                    url: "#",
                },
                {
                    productImg: "buy-comics-merchandise.png",
                    label: "DS Merchandise",
                    url: "#",
                },
                {
                    productImg: "buy-comics-subscriptions.png",
                    label: "Subscriptions",
                    url: "#",
                },
                {
                    productImg: "buy-comics-shop-locator.png",
                    label: "Comic Shop Locator",
                    url: "#",
                },
                {
                    productImg: "buy-dc-power-visa.svg",
                    label: "Dc Power Visa",
                    url: "#",
                },

            ]

        };

    },

    methods: {
        getImage(type) {
            return new URL(`../assets/img/${type}`, import.meta.url).href;
        },

    },
}

</script>

<template>
    <div class="sections">
        <ul>
            <li v-for="section, index in sections" :key="section.label">
                <div class="section">
                    <img :src="getImage(section.productImg)" alt="Section Icon" :id="(index == 3) ? 'measure' : ''">
                    <span> {{ section.label }}</span>
                </div>
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/_variable.scss' as *;

.sections {
    background-color: $primary;
    display: flex;
    justify-content: center;
    padding: 2rem 4rem;
}

ul {
    display: flex;
    flex-direction: row;
    gap: 4rem;
    list-style-type: none;
    align-items: center;
    justify-content: center;

    li {
        text-transform: uppercase;
        color: white;
        font-size: 0.9rem;
        width: 12%;

        .section {
            display: flex;
            align-items: center;

            img {
                width: 23%;
                min-width: 50px;
                margin-right: 1rem;
            }
        }

    }
}

#measure {
    width: 10px;
}
</style>
