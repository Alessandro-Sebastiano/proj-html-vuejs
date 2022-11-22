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
                <CardForm />
            </div>
        </div>
    </div>
</template>

<script>
import ButtonComponent from '../ButtonComponent.vue';
import CardForm from '../CardForm.vue';

export default {
    name: 'HeroComponent',

    components: {
        ButtonComponent,
        CardForm,
    }
}
</script>

<style lang="scss" scoped>
@use '../../assets/styles/partials/variables' as *;

.hero {
    width: 100%;
    padding-top: 84px;
    padding-bottom: 174px;
    background-image: url(/images/marketing-intro.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center center;
    background-attachment: local;


    .container {
        display: flex;
        align-items: flex-start;
        justify-content: flex-start;



        .hero-text-section {
            width: 55%;
            color: $ligth;
            padding-right: 80px;


            h1 {
                font-size: 4.2rem;
                font-weight: 500;
                margin-bottom: 22px;
            }

            p {
                font-size: 1.6rem;
            }


            .button {
                background-color: $ligth;
                color: $dark;
                border: 2px solid $dark;
                margin: 38px 0;
                transition: all 0.2s ease-in-out;

                &:hover {
                    background-color: transparent;
                    border: 2px solid $ligth;
                    color: $ligth;
                }
            }
        }


        .hero-form-section {
            position: relative;
            padding-left: 26px;


            .card-box {
                position: absolute;
                left: 0;
            }
        }


    }
}
</style>