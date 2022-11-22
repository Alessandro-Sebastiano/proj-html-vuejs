<template>
  <HeaderComponent />
  <MainComponent />
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';


export default {
  components: {
    HeaderComponent,
    MainComponent,
  }
}
</script>

<style lang="scss">
.container {
  width: 1265px;
  margin: auto;
}
</style>