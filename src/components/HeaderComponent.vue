<template>
    <div class="header">
        <NavBar />
    </div>
</template>

<script>
import NavBar from './header-subComponent/NavBar.vue';

export default {
    name: 'HeaderComponent',

    components: {
        NavBar,
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;

.header {
    width: 100%;
    padding: 18px;
    border: 1px solid red;
    background-color: $ligth;
    display: flex;
    align-items: center;
    justify-content: center;
}
</style>