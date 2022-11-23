<template>
    <div class="container">
        <div class="contact-box">
            <div class="contact-info">
                <div class="contact-image">
                    <img src="/images/marketing-expert-cta.png" alt="">
                </div>
                <div class="contact-info-text">
                    <h4>Sandy Reiff</h4>
                    <span>Marketing Consultant Expert</span>
                </div>
                <p>Drive Leads and Sales with Avada</p>
            </div>
            <PhoneNumber />
        </div>
    </div>
</template>

<script>
import PhoneNumber from '../PhoneNumber.vue';

export default {
    name: 'ContactComponent',

    components: {
        PhoneNumber,
    }
}
</script>

<style lang="scss" scoped>
@use '../../assets/styles/partials/variables' as *;

.container {
    padding: 110px 0;
}

.contact-box {
    width: 100%;
    padding: 14px 42px;
    box-shadow: 2px 2px 6px 0px rgba(0, 0, 0, 0.44);
    border-radius: 8px;
    display: flex;
    align-items: center;
    justify-content: space-between;


    .contact-info {
        display: flex;
        align-items: center;


        .contact-image {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            overflow: hidden;
            margin-right: 20px;

            img {
                width: 100%;
                height: 100%;
                display: block;
            }
        }


        .contact-info-text {

            h4 {
                font-size: 1.2rem;
                font-weight: 500;
            }

            span {
                font-size: 0.9rem;
            }
        }


        p {
            margin: 0 70px;
            font-size: 1.5rem;
            font-weight: 500;
        }

    }


    .phone-box {
        background-color: $op-orange;
        color: $orange;
        padding: 15px 40px;
        cursor: pointer;
        transition: all 0.2s ease-in-out;


        &:hover {
            background-color: $dark-orange;
            color: $ligth;
        }

    }

}
</style>