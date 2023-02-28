<script>
import AppHeader from './components/AppHeader.vue';
import AppJumbotron from './components/AppJumbotron.vue';
import AppMain from './components/AppMain.vue';
import AppSections from './components/AppSections.vue';
import AppFooter from './components/AppFooter.vue';
import FooterSocial from './components/FooterSocial.vue';
export default {
  components: { AppHeader, AppMain, AppSections, AppFooter, FooterSocial, AppJumbotron }
};
</script>

<template>
  <AppHeader />
  <AppJumbotron />
  <AppMain />
  <AppSections />
  <AppFooter />
  <FooterSocial />
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Titillium+Web:wght@200;400;600;900&display=swap');

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-family: 'Titillium Web', sans-serif;
}

img {
  max-width: 100%;
}

.container {
  max-width: 1300px;
  margin: 0 auto;
}
</style>
