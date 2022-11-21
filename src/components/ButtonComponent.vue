<template>
    <div class="button">
        <span>{{ btnText }}</span>
    </div>
</template>

<script>
export default {
    name: 'ButtonComponent',

    props: ['btnText'],
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

.button {
    display: inline-block;
    padding: 8px 24px;
    border-radius: 6px;
    background-color: $orange;
    cursor: pointer;


    span {
        color: $ligth;
        font-size: 14px;
        font-weight: 700;
    }
}
</style>