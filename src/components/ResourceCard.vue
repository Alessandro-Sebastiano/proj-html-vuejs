<template>
    <div class="resource-card">
        <div class="resource-card-image">
            <div class="overlay"></div>
            <img :src="'/images/' + resourceImg" alt="resource-image">
        </div>
        <span><a href="#">{{ resourceText }}</a></span>
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
        position: relative;

        .overlay {
            position: absolute;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            background: rgb(255, 255, 255);
            background: linear-gradient(180deg, rgba(255, 255, 255, 0) 0%, rgba(226, 92, 14, 0.3785889355742297) 100%);
            opacity: 0;
            transition: all 0.6s ease-in-out;
        }

        &:hover {
            .overlay {
                opacity: 1;
            }
        }


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