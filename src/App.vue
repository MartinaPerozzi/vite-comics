<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppSections from './components/AppSections.vue';
export default {
  components: { AppHeader, AppMain, AppSections }
};
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppSections />
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Titillium+Web:wght@200;400;600;900&display=swap');



* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

img {
  max-width: 100%;
}
</style>
