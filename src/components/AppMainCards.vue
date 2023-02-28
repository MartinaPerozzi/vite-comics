<script>
export default {
    props: {
        cards: Array,
    },
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
        </div>


    </div>
</template>

<style lang="scss" scoped>
.thumbs {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    width: calc (100% % 6);
    list-style-type: none;

    li {
        max-width: 200px;
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
    padding-top: 1rem;
}
</style>