<template>
    <div class="main">
        <HeroComponent />
        <ConsultantComponent />
        <BrandComponent />
    </div>
</template>

<script>
import HeroComponent from './main-subComponent/HeroComponent.vue';
import ConsultantComponent from './main-subComponent/ConsultantComponent.vue';
import BrandComponent from './main-subComponent/BrandComponent.vue';


export default {
    name: 'MainComponent',

    components: {
        HeroComponent,
        ConsultantComponent,
        BrandComponent,
    },
}
</script>

<style lang="scss" scoped>
.main {
    width: 100%;
}
</style>