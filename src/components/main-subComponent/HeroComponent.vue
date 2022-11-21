<template>
    <div class="hero">
        <div class="container">
            <div class="hero-text-section">
                <h1>Unlock Your Online Growth Potential</h1>
                <p>Online marketing to secure customer retention,
                    leads, and sales. We focus on the bigger picture.</p>
                <ButtonComponent btnText="Our Services" />
            </div>
            <div class="hero-form-section">

            </div>
        </div>
    </div>
</template>

<script>
import ButtonComponent from '../ButtonComponent.vue';

export default {
    name: 'HeroComponent',

    components: {
        ButtonComponent,
    }
}
</script>

<style lang="scss" scoped>
@use '../../assets/styles/partials/variables' as *;

.hero {
    width: 100%;
    padding-top: 84px;
    padding-bottom: 134px;
    background-image: url(/images/marketing-intro.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center 0;


    .container {
        display: flex;
        align-items: flex-start;
        justify-content: flex-start;



        .hero-text-section {
            width: 50%;
            padding-right: 86px;
            color: $ligth;


            h1 {
                font-size: 2.8rem;
                margin: 22px 0;
            }

            p {
                font-size: 1.2rem;
            }


            .button {
                background-color: $ligth;
                color: $dark;
                border: 2px solid $ligth;
                margin: 38px 0;
                transition: all 0.4s ease-in-out;

                &:hover {
                    background-color: transparent;
                }
            }
        }
    }
}
</style>