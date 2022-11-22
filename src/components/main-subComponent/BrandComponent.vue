<template>
    <div class="container">
        <div class="brand-box">
            <h2>Some Brands We WorkWith</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
            <div class="brands">
                <div class="brand-logo" v-for="item in brandList">
                    <img :src="'/brands/' + item" alt="brand-logo">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'BrandComponent',

    data() {
        return {

            brandList: ['abstract.png', 'cglobal.png', 'next.png', 'hemisferio.png', 'spaces.png', 'digitalbox.png'],

        }
    }
}
</script>

<style lang="scss" scoped>
.brand-box {
    text-align: center;
    padding: 34px 0;


    h2 {
        font-size: 3rem;
        margin-bottom: 14px;
    }

    p {
        font-size: 1.3rem;
    }

    .brands {
        display: flex;
        align-items: center;
        justify-content: space-between;
        margin-top: 38px;


        .brand-logo {
            width: 140px;

            img {
                width: 100%;
                display: block;
            }
        }
    }

}
</style>