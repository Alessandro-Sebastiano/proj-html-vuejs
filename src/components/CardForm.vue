<template>
    <div class="card-box">
        <div class="card-image">
            <img src="/images/marketing-consultant-expert.jpg" alt="">
        </div>
        <div class="card-text">
            <h3>Richard Madsen</h3>
            <span>Marketing Consultant Expert</span>
            <PhoneNumber />
        </div>
        <div class="form-section">
            <form>
                <input type="text" placeholder="Your Name*">
                <input type="text" placeholder="Your Email*">
                <input type="text" placeholder="Your Phone Number*">
                <ButtonComponent btnText="Get Callback" />
            </form>
        </div>
        <div class="term">
            <span>By submitting my data i agree to be contacted</span>
        </div>
    </div>
</template>

<script>
import PhoneNumber from './PhoneNumber.vue';
import ButtonComponent from './ButtonComponent.vue';

export default {
    name: 'CardForm',

    components: {
        PhoneNumber,
        ButtonComponent,
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

.card-box {
    width: 415px;
    padding: 38px 27px;
    border-radius: 12px;
    background-color: $ligth;
    box-shadow: 2px 2px 6px 0px rgba(0, 0, 0, 0.44);


    .card-image {
        width: 82px;
        height: 82px;
        border-radius: 50%;
        overflow: hidden;
        margin: auto;

        img {
            width: 100%;
            height: 100%;
            display: block;
        }
    }



    .card-text {
        text-align: center;

        h3 {
            margin: 8px 0;
            font-size: 1.4rem;
            font-weight: 600;
        }

        span {
            display: block;
            margin-bottom: 8px;
        }

        .phone-box {
            color: $orange;
            justify-content: center;
        }
    }



    .form-section {
        width: 100%;


        input {
            display: block;
            width: 100%;
            padding: 18px;
            border-radius: 8px;
            margin: 16px 0;
            border: 1px solid $grey;
            font-size: 1rem;

            &:focus {
                outline: none;
                border: 2px solid $grey;
            }
        }


        .button {
            display: block;
            text-align: center;
            padding: 18px 0;
        }
    }

    .term {
        span {
            display: block;
            font-size: 0.7rem;
            margin-top: 12px;
            text-align: center;
        }
    }

}
</style>