<template>
    <div class="main">
        <HeroComponent />
        <ConsultantComponent />
        <BrandComponent />
        <ContactComponent />
        <CaseStudies />
    </div>
</template>

<script>
import HeroComponent from './main-subComponent/HeroComponent.vue';
import ConsultantComponent from './main-subComponent/ConsultantComponent.vue';
import BrandComponent from './main-subComponent/BrandComponent.vue';
import ContactComponent from './main-subComponent/ContactComponent.vue';
import CaseStudies from './main-subComponent/CaseStudies.vue';


export default {
    name: 'MainComponent',

    components: {
        HeroComponent,
        ConsultantComponent,
        BrandComponent,
        ContactComponent,
        CaseStudies,
    },
}
</script>

<style lang="scss" scoped>
.main {
    width: 100%;
}
</style>