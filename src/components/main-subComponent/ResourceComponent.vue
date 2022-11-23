<template>
    <div class="resource-box">
        <div class="container">
            <div class="initial-box">
                <h2>Marketing Resources: Insider Advice on How to Increase Online Sales</h2>
                <ButtonComponent btnText="Explore All Resource" />
            </div>
            <div class="cards-box">
                <ResourceCard v-for="item in resourceCardsList" :resourceImg="item.image" :resourceText="item.text" />
            </div>
        </div>
    </div>
</template>

<script>
import ButtonComponent from '../ButtonComponent.vue';
import ResourceCard from '../ResourceCard.vue';

export default {
    name: 'ResourceComponent',

    components: {
        ButtonComponent,
        ResourceCard,
    },

    data() {
        return {
            resourceCardsList: [
                {
                    image: 'blog-posts-6.jpg',
                    text: 'Marketing Tips And Tricks For Your Website',
                },
                {
                    image: 'blog-posts-5.jpg',
                    text: 'How to Write Stunning Blog Post Titles',
                },
                {
                    image: 'blog-posts-4.jpg',
                    text: 'Techniques to Reduce Facebook Ads Spend',
                },
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../../assets/styles/partials/variables' as *;

.resource-box {
    background-color: $background;
    padding: 95px 0;
}


.initial-box {
    position: relative;

    h2 {
        font-size: 3rem;
        font-weight: 500;
        width: 50%;
    }

    .button {
        position: absolute;
        bottom: 0;
        right: 0;
    }
}



.cards-box {
    margin-top: 88px;
    display: flex;
    align-items: center;
    justify-content: space-between;
}
</style>