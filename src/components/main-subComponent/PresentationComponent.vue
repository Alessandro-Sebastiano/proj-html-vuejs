<template>
    <div class="presentation-box">
        <div class="container">
            <div class="first-section">
                <div class="first-section-text">
                    <h2>We Boost Our Clients' Bottom Line by Optimizing Their Growth Potential.</h2>
                    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ipsam voluptatem eius itaque obcaecati
                        adipisci rem voluptatibus deleniti reprehenderit laboriosam alias!</p>
                    <ButtonComponent btnText="Why Work With Us" />
                </div>
                <div class="first-section-image">
                    <img src="/images/we-boost-our-clients.jpg" alt="we-boost">
                </div>
            </div>
            <div class="second-section">
                <div class="second-section-text">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import ButtonComponent from '../ButtonComponent.vue';

export default {
    name: 'PresentationComponent',

    components: {
        ButtonComponent,
    }
}
</script>

<style lang="scss" scoped>
@use '../../assets/styles/partials/variables' as *;

.presentation-box {
    width: 100%;
    padding: 90px 0;
    background-color: $background;
}

.first-section {
    display: flex;
    align-items: center;


    .first-section-text {
        width: 50%;
        padding-right: 160px;

        h2 {
            font-size: 3rem;
            font-weight: 500;
        }

        p {
            font-size: 1.3rem;
            margin: 28px 0;
        }
    }


    .first-section-image {
        width: 50%;
        border-radius: 10px;
        overflow: hidden;

        img {
            width: 100%;
            display: block;
        }
    }
}
</style>