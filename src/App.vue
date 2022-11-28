<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";

export default {
  components: {
    AppHeader,
    AppMain,
  },
};
</script>

<template>
  <div class="background">
    <AppHeader />
    <AppMain />
  </div>
</template>

<style lang="scss">
@import "./style/global.scss";

.background {
  background-color: #2e3a46;
}
</style>
