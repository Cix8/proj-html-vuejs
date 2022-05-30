<template>
  <div id="app">
    <AppHeader :linksArray="headerNavLinks" />
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";

export default {
  name: "App",
  components: {
    AppHeader,
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
