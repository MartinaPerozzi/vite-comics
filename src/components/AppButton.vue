<script>
export default {
    props: {
        buttonText: String,
    },
}
</script>

<template>
    <div class="bg">
        <button type="button">{{ buttonText }}</button>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/_variable.scss' as *;

button {
    background-color: $primary;
    padding: 0.5rem 1rem;
    border: none;
    color: white;
    font-weight: 500;
}
</style>