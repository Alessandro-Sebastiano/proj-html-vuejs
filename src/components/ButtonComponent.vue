<template>
    <div class="button">
        <span><a href="#">{{ btnText }}</a></span>
        <i class="fa-solid fa-arrow-right" v-if="btnText == 'Our Services'"></i>
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
        font-size: 14px;
        font-weight: 700;
    }

    i {
        vertical-align: middle;
        margin-left: 12px;
    }
}
</style>