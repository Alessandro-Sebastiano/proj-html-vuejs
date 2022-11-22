<template>
    <div class="consultant-card-box">
        <div class="consultant-card-image">
            <img :src="img" alt="consultant-svg">
        </div>
        <div class="consultant-card-text">
            <div class="title">
                <span class="circle" :class="color">

                </span>
                <span>{{ cardTitle }}</span>
            </div>
            <h2>{{ cardDescription }}</h2>
            <p>{{ cardText }}</p>
            <ButtonComponent btnText="Get a Consultation" />
        </div>
    </div>
</template>

<script>
import ButtonComponent from './ButtonComponent.vue';

export default {
    name: 'ConsultantCard',

    components: {
        ButtonComponent,
    },

    props: ['img', 'cardTitle', 'cardDescription', 'cardText', 'color'],
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

.consultant-card-box {
    display: flex;
    align-items: center;
    padding: 68px 0;
}


.consultant-card-image {
    width: 50%;
    padding: 18px;

    img {
        width: 100%;
        display: block;
    }
}

.consultant-card-text {
    width: 50%;
    padding: 22px 128px;

    .title {
        display: flex;
        align-items: center;
        margin-bottom: 8px;


        .circle {
            display: inline-block;
            width: 34px;
            height: 34px;
            border-radius: 50%;
            margin-right: 8px;

        }

        .blue {
            background-color: $blue;
        }


        .yellow {
            background-color: $yellow;
        }


        .green {
            background-color: $ligth-green;
        }


        span {
            font-size: 1.1rem;
            font-weight: 600;
        }

    }




    h2 {
        font-size: 2.6rem;
        font-weight: 600;
    }


    p {
        font-size: 1.2rem;
        font-weight: 500;
        margin: 26px 0;
    }
}
</style>