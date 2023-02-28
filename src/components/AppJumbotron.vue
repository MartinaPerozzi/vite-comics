<script>
export default {

}
</script>

<template>
    <div class="bg">

        <div class="tag">
            <span>CURRENT SERIES</span>
        </div>


    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/_variable.scss' as *;

.bg {
    background-image: url(../assets/img/jumbotron.jpg);
    width: 100%;
    height: 380px;
    background-size: cover;
    background-position: top;
    background-repeat: no-repeat;
    position: relative;

    .tag {
        position: absolute;
        background-color: $primary;
        padding: 0.5rem 2rem;
        color: white;
        font-size: 1.4rem;
        font-weight: 600;
        top: 355px;
        left: 260px;

    }

}
</style>