<template>
    <div class="container">
        <div class="footer-first-section">
            <div class="footer-text-section">
                <h3>Grow Your Online Business Strategically, and Improve Customer Retention.</h3>
                <div class="icons">
                    <a href="#"><i :class="item" v-for="item in iconsList"></i></a>
                </div>
            </div>
            <div class="footer-menu-section">
                <div class="menu-box" v-for="(item, index) in menuList">
                    <span class="menu-box-title">{{ item.title }}</span>
                    <ul>
                        <li v-for="item in menuList[index].items"><a href="#">{{ item }}</a></li>
                    </ul>
                </div>
            </div>
        </div>
        <div class="footer-second-section">
            <span>© 2020 • Avada Consultant • Powered by WordPress</span>
            <span>Call Us (555) 802-1234</span>
            <span>info@yourcompany.com</span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'FooterComponent.vue',

    data() {
        return {
            menuList: [
                {
                    title: 'Services',
                    items: ['Marketing Plan', 'Sales Development', 'Digital Marketing', 'Pricing', 'Why Us', 'Case Studies'],
                },
                {
                    title: 'Resources',
                    items: ['Learning Center', 'Video Tutorials', 'Customers', 'Blog'],
                },
                {
                    title: 'Company',
                    items: ['Who We Are', 'Contact Us', 'Careers'],
                },
            ],

            iconsList: ['fa-brands fa-facebook-f', 'fa-brands fa-twitter', 'fa-brands fa-instagram', 'fa-brands fa-youtube', 'fa-brands fa-linkedin-in', 'fa-brands fa-tiktok'],
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

.container {
    padding: 90px 0;
}

.footer-first-section {
    width: 100%;
    display: flex;
    align-items: flex-start;

    .footer-text-section {
        width: 40%;
        padding: 0 40px;

        h3 {
            font-size: 1.8rem;
            font-weight: 500;
        }

        .icons {
            margin-top: 26px;

            i {
                font-size: 1.4rem;
                color: $dark;
                margin-right: 18px;
            }
        }
    }



    .footer-menu-section {
        width: 60%;
        display: flex;
        align-items: flex-start;
        justify-content: space-between;
        padding: 0 32px;

        .menu-box {
            flex-grow: 1;
            margin-right: 44px;

            .menu-box-title {
                font-size: 1.3rem;
                font-weight: 500;
                display: block;
                margin-bottom: 17px;
            }

            ul {
                list-style: none;


                li {
                    padding: 2px 0;
                    margin-bottom: 12px;
                    position: relative;
                    cursor: pointer;

                    &:after {
                        content: '';
                        width: 2px;
                        height: 100%;
                        position: absolute;
                        display: block;
                        top: 0;
                        right: 4px;
                        background-color: $orange;
                        transform: scale(0);
                        transition: all 0.2s ease-in-out;
                        transition-delay: 0.1s;
                    }

                    &:hover {
                        color: $orange;

                        &:after {
                            transform: scale(1);
                            right: -2px;
                        }
                    }
                }
            }

        }
    }


}


.footer-second-section {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-top: 80px;
}
</style>