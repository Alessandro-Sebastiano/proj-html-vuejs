<template>
    <div class="card-box">
        <div class="card-image">
            <div class="overlay"></div>
            <img :src="'/images/' + caseImg" alt="">
            <div class="overlay"></div>
        </div>
        <p>{{ caseText }}</p>
        <div class="card-text">
            <span class="large">{{ caseInfo1 }}</span>
            <span>{{ caseInfo2 }}</span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CaseCard',

    props: ['caseImg', 'caseText', 'caseInfo1', 'caseInfo2'],
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

.card-box {
    max-width: 500px;
    text-align: left;

    .card-image {
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
                opacity: 0.8;
            }
        }

        img {
            width: 100%;
            display: block;
        }
    }


    p {
        font-size: 1.4rem;
        font-weight: 500;
        padding: 20px 0;
        border-bottom: 1px dashed $grey;
    }

    .card-text {
        padding: 12px 0;

        span {
            display: block;
        }

        .large {
            font-size: 2.8rem;
            font-weight: 700;
        }
    }

}
</style>