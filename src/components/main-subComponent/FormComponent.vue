<template>
    <div class="form-box">
        <div class="container">
            <div class="text-box">
                <div class="section border">
                    <h2>Let's Make Things Happen</h2>
                    <p>Curabitur ac leo nunc. Vestibulum et mauris vel ante finibus maximus nec ut leo. Integer
                        consectetur.
                    </p>
                </div>
                <div class="section">
                    <p class="cit">
                        “The team at Avada Marketing Consultant is fabulous. They helped us unlock our potential online
                        and
                        offline. We have experienced year on year growth due to their progressive approach.”</p>
                    <span class="name">George Anderson</span>
                    <span>Digitalbox CEO</span>
                </div>
            </div>
            <div class="form">
                <CardForm />
            </div>
        </div>
    </div>
</template>

<script>
import CardForm from '../CardForm.vue';

export default {
    name: 'FormComponent',

    components: {
        CardForm,
    }
}
</script>

<style lang="scss" scoped>
@use '../../assets/styles/partials/variables' as *;

.form-box {
    width: 100%;
    background-color: $dark;
    padding: 110px 0;
}

.container {
    display: flex;
    align-items: flex-start;


    .text-box {
        width: 50%;
        color: $ligth;
        padding-right: 120px;


        .section {
            padding: 20px 0;
            position: relative;
        }

        .border {
            &::after {
                content: '';
                display: block;
                width: 140px;
                height: 1px;
                background-color: $dark-grey;
                position: absolute;
                bottom: -1px;
            }
        }

        h2 {
            font-size: 3rem;
        }

        p {
            font-size: 1.6rem;
            margin: 30px 0;
        }

        .cit {
            font-size: 1.4rem;
        }

        .name {
            font-size: 1.2rem;
            color: $ligth;
        }

        span {
            display: block;
            margin-bottom: 10px;
            color: $dark-grey;
        }
    }
}
</style>