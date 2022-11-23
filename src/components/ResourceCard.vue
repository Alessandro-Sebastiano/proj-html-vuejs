<template>
    <div class="resource-card">
        <div class="resource-card-image">
            <img :src="'/images/' + resourceImg" alt="resource-image">
        </div>
        <span>{{ resourceText }}</span>
    </div>
</template>

<script>
export default {
    name: 'ResourceCard',
    props: ['resourceImg', 'resourceText'],
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

.resource-card {
    max-width: 400px;

    .resource-card-image {
        width: 100%;
        cursor: pointer;


        img {
            width: 100%;
            display: block;
        }
    }

    span {
        display: block;
        margin-top: 20px;
        font-size: 1.8rem;
        font-weight: 500;
        cursor: pointer;
        transition: all 0.2s ease-in-out;

        &:hover {
            color: $orange;
        }
    }

}
</style>