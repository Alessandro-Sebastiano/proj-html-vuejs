<template>
    <div class="presentation-box">
        <div class="container">
            <div class="first-section">
                <div class="first-section-text">
                    <h2>We Boost Our Clients' Bottom Line by Optimizing Their Growth Potential.</h2>
                    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ipsam voluptatem eius itaque obcaecati
                        adipisci rem voluptatibus deleniti reprehenderit laboriosam alias!</p>
                    <ButtonComponent btnText="Why Work With Us" />
                </div>
                <div class="first-section-image">
                    <img src="/images/we-boost-our-clients.jpg" alt="we-boost">
                </div>
            </div>
            <div class="second-section">
                <div class="second-section-text">
                    <div class="text-style" v-for="item in presentationList">
                        <h3>{{ item.title }}</h3>
                        <p>{{ item.text }}</p>
                    </div>
                </div>
                <div class="icons-section">
                    <div class="item" v-for="item in itemIconList">
                        <span class="icon-box">
                            <i class="fa-solid fa-square-plus"></i>
                        </span>
                        <span class="item-text">
                            <h4>{{ item.itemTitle }}</h4>
                            <span>{{ item.itemText }}</span>
                        </span>
                    </div>
                </div>
            </div>
            <div class="awards">
                <h3>Awards</h3>
                <div class="awards-container">
                    <div class="award-box" v-for="item in awardsList">
                        <div class="award-logo">
                            <img :src="'/awards/' + item.logo" alt="">
                        </div>
                        <span>{{ item.text1 }}</span>
                        <span>{{ item.text2 }}</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import ButtonComponent from '../ButtonComponent.vue';

export default {
    name: 'PresentationComponent',

    components: {
        ButtonComponent,
    },


    data() {
        return {
            presentationList: [
                {
                    title: 'We Build Relationship',
                    text: 'Curabitur ac leo nunc. Vestibulum et mauris vel ante finibus maximus nec ut leo. Integer consectetur.',
                },
                {
                    title: 'Proprietary Processes',
                    text: 'Curabitur ac leo nunc. Vestibulum et mauris vel ante finibus maximus nec ut leo. Integer consectetur.',
                },
            ],

            itemIconList: [
                {
                    itemTitle: 'Accountability',
                    itemText: 'Curabitur ac leo nunc vestibulum',
                },
                {
                    itemTitle: 'Transparency',
                    itemText: 'Curabitur ac leo nunc vestibulum',
                },
                {
                    itemTitle: 'Investment',
                    itemText: 'Curabitur ac leo nunc vestibulum',
                },
            ],

            awardsList: [
                {
                    logo: 'award-a.png',
                    text1: 'Winner Seo Master MAGT',
                    text2: 'Smart Start Award 2017',
                },
                {
                    logo: 'award-b.png',
                    text1: 'Top Social Media Agencies',
                    text2: 'Next Partner 2018',
                },
                {
                    logo: 'award-c.png',
                    text1: '10 Fastest Growing Abstract',
                    text2: 'Solution Providers 2019',
                },
                {
                    logo: 'award-d.png',
                    text1: 'National Excellence Agencie',
                    text2: 'Award Winner 2020',
                },
            ],
        }
    }

}
</script>

<style lang="scss" scoped>
@use '../../assets/styles/partials/variables' as *;

.presentation-box {
    width: 100%;
    padding: 90px 0;
    background-color: $background;
}

.first-section {
    display: flex;
    align-items: center;


    .first-section-text {
        width: 50%;
        padding-right: 160px;

        h2 {
            font-size: 3rem;
            font-weight: 500;
        }

        p {
            font-size: 1.3rem;
            margin: 28px 0;
        }
    }


    .first-section-image {
        width: 50%;
        border-radius: 10px;
        overflow: hidden;

        img {
            width: 100%;
            display: block;
        }
    }
}


.second-section {
    display: flex;
    align-items: center;
    padding: 80px 0;


    .second-section-text {
        width: 50%;
        padding-right: 160px;


        .text-style {
            margin-bottom: 40px;

            h3 {
                font-size: 1.8rem;
                margin-bottom: 20px;
            }

            p {
                font-size: 1.2rem;
            }
        }
    }


    .icons-section {
        padding: 0 30px;

        .item {
            display: flex;
            align-items: center;
            margin-bottom: 42px;


            .icon-box {
                padding: 15px 20px;
                border: 2px solid $orange;
                border-radius: 16px;
                color: $orange;
                font-size: 1.8rem;
                margin-right: 16px;
            }

            .item-text {
                h4 {
                    font-size: 1.4rem;
                    margin-bottom: 14px;
                    transition: all 0.2s ease-in-out;

                    &:hover {
                        color: $orange;
                    }
                }

                span {
                    font-size: 1.2rem;
                }
            }
        }
    }

}



.awards {
    text-align: center;

    h3 {
        font-size: 1.8rem;
    }

    .awards-container {
        display: flex;
        align-items: center;
        justify-content: space-between;
        margin-top: 40px;



        .award-box {
            padding: 0 20px;

            .award-logo {
                width: 160px;
                margin: 0 auto;

                img {
                    width: 100%;
                    display: block;
                }
            }

            span {
                font-size: 1.2rem;
                display: block;
                margin-bottom: 8px;
            }
        }
    }
}
</style>