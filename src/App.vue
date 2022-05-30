<template>
  <div id="app">
    <AppHeader :linksArray="headerNavLinks" />
    <AppJumbo />
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppJumbo from "./components/AppJumbo.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    AppJumbo,
  },
  data() {
    return {
      headerNavLinks: ["Home", "Pages", "Courses", "Features", "Blog", "Shop"],
    };
  },
};
</script>

<style lang="scss">
@import "./style/common.scss";
</style>
