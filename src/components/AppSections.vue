<script>
export default {
    data() {
        return {
            sections: [
                {
                    productImg: "buy-comics-digital-comics",
                    label: "Digital Comics",
                    link: "#",
                },
                {
                    productImg: "buy-comics-merchandise",
                    label: "DS Merchandise",
                    link: "#",
                },
                {
                    productImg: "buy-comics-subscriptions",
                    label: "Subscriptions",
                    link: "#",
                },
                {
                    productImg: "buy-comics-shop-locator",
                    label: "Comic Shop Locator",
                    link: "#",
                },
                {
                    productImg: "buy-dc-power-visa",
                    label: "Dc Power Visa",
                    link: "#",
                },

            ]

        };

    },


    methods: {
        getImage(type) {

            let lastElement = this.sections.length - 1;
            if (lastElement) {
                return new URL(`../assets/img/${type}.svg`, import.meta.url).href;
            } else {
                return new URL(`../assets/img/${type}.png`, import.meta.url).href;
            }
        },

    },
}

</script>

<template>
    <div>
        <ul>
            <li v-for="section in sections" :key="section.label">
                <img :src="getImage(section.productImg)" alt="Section Icon">
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
ul {
    display: flex;
    flex-direction: row;
    gap: 2rem;
    list-style-type: none;
}
</style>
