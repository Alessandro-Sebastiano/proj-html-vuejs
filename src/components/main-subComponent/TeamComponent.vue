<template>
    <div class="container">
        <div class="team-box">
            <div class="team-image">
                <img src="/images/large-testimonial.jpg" alt="testimonial">
            </div>
            <div class="team-text">
                <p>“The team at Avada Marketing Consultant is fabulous. They helped us unlock our potential online and
                    offline. We have experienced year on year growth due to their progressive approach.”</p>
                <span class="name">Kate Schadler</span>
                <span>Marketing Consultant - Abstract</span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'TeamComponent',
}
</script>

<style lang="scss" scoped>
.team-box {
    display: flex;
    align-items: center;
    padding: 90px 0;


    .team-image {
        width: 50%;
        border-radius: 8px;
        overflow: hidden;


        img {
            width: 100%;
            display: block;
        }
    }

    .team-text {
        width: 50%;
        padding: 0 120px;


        p {
            font-size: 1.8rem;
            font-weight: 500;
            margin-bottom: 28px;
        }


        .name {
            font-size: 1.2rem;
            margin-bottom: 10px
        }

        span {
            display: block;
        }
    }
}
</style>