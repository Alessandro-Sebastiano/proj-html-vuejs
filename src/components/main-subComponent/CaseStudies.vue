<template>
    <div class="container">
        <div class="case-box">
            <h2>Trusted By Leading Organizations</h2>
            <div class="case-cards-box">
                <CaseCard v-for="(item, index) in caseCardList" :caseImg="item.caseImage" :caseText="item.caseCardText"
                    :caseInfo1="item.caseCardInfo1" :caseInfo2="item.caseCardInfo2" />
            </div>
            <ButtonComponent btnText="Read More Case Studies" />
        </div>
    </div>
</template>

<script>
import CaseCard from '../CaseCard.vue';
import ButtonComponent from '../ButtonComponent.vue';

export default {
    name: 'CaseStudies',

    components: {
        CaseCard,
        ButtonComponent,
    },


    data() {
        return {
            caseCardList: [
                {
                    caseImage: 'case-studies-1.jpg',
                    caseCardText: 'How Spaces attracted five milion visitors by improving te content',
                    caseCardInfo1: '200%',
                    caseCardInfo2: 'Higer revenue from digital',
                },

                {
                    caseImage: 'case-studies-4.jpg',
                    caseCardText: 'Creativity Helped Hemisferio to increase their brand reach vertically',
                    caseCardInfo1: '10x',
                    caseCardInfo2: 'Sales increase with the same ad spend',
                },

                {
                    caseImage: 'case-studies-6.jpg',
                    caseCardText: 'How DigitalBox used AI-powered data insight to boost sales',
                    caseCardInfo1: '3-year',
                    caseCardInfo2: 'Partnership with Avada Consultant',
                },
            ]
        }
    }

}
</script>

<style lang="scss" scoped>
@use '../../assets/styles/partials/variables' as *;

.container {
    padding-bottom: 70px;
}

.case-box {
    text-align: center;


    h2 {
        font-size: 3rem;
        margin-bottom: 60px;
    }


    .case-cards-box {
        display: flex;
        align-items: center;
        justify-content: space-between;

        .card-box {
            width: calc((100% / 3) - 20px);
        }
    }


    .button {
        margin: 40px 0;
    }
}
</style>