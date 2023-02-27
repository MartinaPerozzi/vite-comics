<script>
export default {
    data() {
        return {
            sections: [
                {
                    productImg: "buy-comics-digital-comics.png",
                    label: "Digital Comics",
                    link: "#",
                },
                {
                    productImg: "buy-comics-merchandise.png",
                    label: "DS Merchandise",
                    link: "#",
                },
                {
                    productImg: "buy-comics-subscriptions.png",
                    label: "Subscriptions",
                    link: "#",
                },
                {
                    productImg: "buy-comics-shop-locator.png",
                    label: "Comic Shop Locator",
                    link: "#",
                },
                {
                    productImg: "buy-dc-power-visa.svg",
                    label: "Dc Power Visa",
                    link: "#",
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
.sections {
    background-color: #0182f9;
    display: flex;
    justify-content: center;
    padding: 1rem 4rem;
}

ul {
    display: flex;
    flex-direction: row;
    gap: 2rem;
    list-style-type: none;
    align-items: center;

    li {
        text-transform: uppercase;
        color: white;
        font-size: 0.9rem;

        .section {
            display: flex;
            align-items: center;

            img {
                width: 23%;
                min-width: 50px;
                max-width: 70px;
                margin-right: 1rem;
            }
        }

    }
}

#measure {
    width: 10px;
}

// li:nth-child(4) img {
//     max-width: 10px;
// }
</style>
