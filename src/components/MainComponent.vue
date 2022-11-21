<template>
    <div class="main">
        <HeroComponent />
    </div>
</template>

<script>
import HeroComponent from './main-subComponent/HeroComponent.vue';

export default {
    name: 'MainComponent',

    components: {
        HeroComponent,
    },
}
</script>

<style lang="scss" scoped>
.main {
    width: 100%;
}
</style>