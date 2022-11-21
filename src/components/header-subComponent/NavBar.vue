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
    width: 1105px;
    display: flex;
    align-items: center;
    justify-content: center;


    .logo {
        width: 174px;
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

                a {
                    text-decoration: none;
                    padding: 4px;
                    color: $dark;
                    font-weight: 600;
                    border-bottom: 2px solid $orange;
                    position: relative;

                    &:after {
                        content: '';
                        width: 100%;
                        height: 2px;
                        display: block;
                        position: absolute;
                        bottom: -2px;
                        right: 0;
                        background-color: $ligth;
                    }

                    &:hover {
                        color: $orange;
                    }
                }

                .active {
                    color: $orange;

                    &:after {
                        width: 0px;
                        transition: all 0.4s ease-out;

                    }
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
    }
}
</style>