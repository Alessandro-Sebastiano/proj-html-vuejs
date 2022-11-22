<template>
    <div class="button">
        <a href="#"><span>{{ btnText }}<i class="fa-solid fa-arrow-right"
                    v-if="btnText == 'Our Services'"></i></span></a>
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
    border-radius: 10px;
    background-color: $orange;
    cursor: pointer;
    color: $ligth;

    a {
        padding: 15px 40px;
        display: block;
    }

    span {
        font-size: 18px;
        font-weight: 600;
    }

    i {
        vertical-align: middle;
        margin-left: 12px;
    }
}
</style>