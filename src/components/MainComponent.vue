<template>
    <div class="main">
        <HeroComponent />
        <ConsultantComponent />
    </div>
</template>

<script>
import HeroComponent from './main-subComponent/HeroComponent.vue';
import ConsultantComponent from './main-subComponent/ConsultantComponent.vue';

export default {
    name: 'MainComponent',

    components: {
        HeroComponent,
        ConsultantComponent,
    },
}
</script>

<style lang="scss" scoped>
.main {
    width: 100%;
}
</style>