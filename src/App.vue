<script>
// componenti
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

export default {
  data() {
    return {
    }
  },
  components: {
    AppHeader,
    AppMain
  },
}
</script>

<template>
    <div>
        <!-- header component -->
        <AppHeader />

        <!-- main component -->
         <AppMain/>
    </div>
</template>

<style lang="scss">
@use 'assets/scss/main' as *;
// Import all of Bootstrap's CSS
@import "bootstrap/scss/bootstrap";
</style>
