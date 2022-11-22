<template>
    <div class="container">
        <ConsultantCard v-for="(item, index) in consultantCardList" :img="item.image" :cardTitle="item.title"
            :cardDescription="item.description" :cardText="item.text" :color="item.circleColor"
            :class="item.direction !== '' ? 'reverse' : ''" />
    </div>
</template>

<script>
import ConsultantCard from '../ConsultantCard.vue';

export default {
    name: 'ConsultantComponent',

    components: {
        ConsultantCard,
    },

    data() {
        return {
            consultantCardList: [

                {
                    image: '/svg/img1.svg',
                    title: 'Business Growth',
                    description: 'Increase Brand Awareness',
                    text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cum asperiores sequi ut eum quae consequuntur natus rerum incidunt vel saepe.',
                    direction: '',
                    circleColor: 'blue',
                },

                {
                    image: '/svg/img2.svg',
                    title: 'Investors In People',
                    description: 'In-House Sales Training',
                    text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cum asperiores sequi ut eum quae consequuntur natus rerum incidunt vel saepe.',
                    direction: 'reverse',
                    circleColor: 'yellow',
                },

                {
                    image: '/svg/img3.svg',
                    title: 'Social Media Analysis',
                    description: 'Harness Your Social Proof',
                    text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cum asperiores sequi ut eum quae consequuntur natus rerum incidunt vel saepe.',
                    direction: '',
                    circleColor: 'green',
                },

            ],
        }
    }

}
</script>

<style lang="scss" scoped>
.container {
    padding: 78px 0;
}


.reverse {
    flex-direction: row-reverse;
}
</style>