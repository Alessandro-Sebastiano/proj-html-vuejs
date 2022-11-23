<template>
    <div class="navbar">
        <div class="logo">
            <img :src="logoImg" alt="logo">
        </div>
        <div class="menu">
            <ul>
                <li v-for="(item, index) in menuItem"><a href="#" :class="{ active: item.isActive }"
                        @click="setActive(index)">{{ item.text }}</a>
                </li>
            </ul>
        </div>

        <PhoneNumber />
        <ButtonComponent btnText="Free Quote" />
    </div>
</template>

<script>
import PhoneNumber from '../PhoneNumber.vue';
import ButtonComponent from '../ButtonComponent.vue';

export default {
    name: 'NavBar',

    components: {
        PhoneNumber,
        ButtonComponent,
    },

    data() {
        return {
            logoImg: '/images/avada-marketing-logo.png',
            menuItem: [
                {
                    text: 'Home',
                    subMenu: true,
                    isActive: true,
                },

                {
                    text: 'Services',
                    subMenu: true,
                    isActive: false,
                },

                {
                    text: 'Why Us',
                    subMenu: false,
                    isActive: false,
                },

                {
                    text: 'Case Studies',
                    subMenu: false,
                    isActive: false,
                },

                {
                    text: 'About',
                    subMenu: false,
                    isActive: false,
                },

                {
                    text: 'Blog',
                    subMenu: false,
                    isActive: false,
                },
            ],
        }
    },


    methods: {
        setActive(i) {
            this.menuItem.forEach((el) => {
                el.isActive = false;
            })
            if (!this.menuItem[i].isActive) {
                this.menuItem[i].isActive = true;
            }
        }
    }

}
</script>

<style lang="scss" scoped>
@use '../../assets/styles/partials/variables' as *;

.navbar {
    display: flex;
    align-items: center;
    justify-content: center;


    .logo {
        width: 224px;
        flex-shrink: 0;


        img {
            width: 100%;
            display: block;
        }
    }


    .menu {
        margin: 0 14px;
        flex-shrink: 0;

        ul {
            list-style: none;
            display: flex;
            align-items: center;
            justify-content: center;


            li {
                padding: 0px 16px;
                font-size: 1.1rem;

                a {
                    text-decoration: none;
                    padding: 6px;
                    color: $dark;
                    font-weight: 600;
                    position: relative;
                    transition: all 0.4s ease-in-out;

                    &:after {
                        content: '';
                        width: 100%;
                        height: 2px;
                        display: block;
                        position: absolute;
                        bottom: -2px;
                        background-color: $orange;
                        transform: scale(0);
                        transition: all 0.4s ease-in-out;
                    }

                    &:hover {
                        color: $orange;

                        &:after {
                            transform: scale(1);
                        }
                    }
                }

                .active {
                    color: $orange;

                    border-bottom: 2px solid $orange;
                }
            }
        }
    }

    .phone-box {
        flex-shrink: 0;
    }

    .button {
        margin-left: 12px;
        background-color: $op-orange;
        flex-shrink: 0;
        color: $orange;
        transition: all 0.1s ease-in-out;

        &:hover {
            background-color: $orange;
            color: $ligth;
        }
    }
}
</style>