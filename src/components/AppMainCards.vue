<script>
import AppButton from "./AppButton.vue";
export default {
    data() {
        return {
            loadButton: "LOAD MORE",
        }
    },

    props: {
        cards: Array,
    },

    components: { AppButton },

}
</script>

<template>
    <div class="bg">
        <div class="container">
            <ul class="thumbs">
                <li v-for="card in cards" key="card.thumb">
                    <div class="card-box">
                        <img :src="card.thumb" alt="card image">
                    </div>
                    <div class="card-info">
                        <span>{{ card.series }}</span>
                    </div>
                </li>
            </ul>
            <AppButton :buttonText="loadButton" />
        </div>


    </div>
</template>

<style lang="scss" scoped>
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.thumbs {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 1rem;
    list-style-type: none;

    li {
        max-width: 200px;
        padding-bottom: 2rem;
    }
}

.card-box {
    width: 200px;
    height: 200px;

    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: top;
    }
}

.card-info {
    font-size: 1rem;
    text-transform: uppercase;
    color: white;
    padding-top: 0.5rem;
}
</style>