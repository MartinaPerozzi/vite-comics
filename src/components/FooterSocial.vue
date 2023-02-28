<script>
export default {
    data() {
        return {

            socialLinks: [
                {
                    label: "footer-facebook.png",
                    url: "#",
                },
                {
                    label: "footer-twitter.png",
                    url: "#",
                },
                {
                    label: "footer-periscope.png",
                    url: "#",
                },
                {
                    label: "footer-pinterest.png",
                    url: "#",
                },
                {
                    label: "footer-youtube.png",
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
    <div class="icons-bg">
        <div class="container">
            <div class="icons-right-side">
                <div>
                    <span>SIGN-UP NOW</span>
                </div>
            </div>
            <div class="icons-left-side">
                <span>FOLLOW US</span>
                <div class="icon" v-for="link in socialLinks">
                    <img :src="getImage(link.label)" alt="social Icons">
                </div>
            </div>


        </div>
    </div>
</template>

<style lang= "scss" scoped>
// ICONS
.icons-bg {
    background-color: rgb(35, 35, 35);
    padding: 2rem 4rem;
    color: white;

    .container {
        display: flex;
        justify-content: space-between;
    }


    .icons-right-side {
        div {
            border: 1px solid #0182f9;
            padding: 0.5rem 1rem;
        }
    }

    .icons-left-side {
        display: flex;
        gap: 1rem;
        align-items: center;
        color: #0182f9;

    }
}
</style>
