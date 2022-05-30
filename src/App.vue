<template>
  <div id="app">
    <AppHeader :linksArray="headerNavLinks" />
    <AppJumbo />
    <main>
      <section class="starting">
        <div class="title">
          <div class="secondary-title">
            <span>START LEARNING CODING LANGUAGE</span>
          </div>
          <div class="primary-title">
            <h2>Build Your Dream <span>TODAY</span></h2>
          </div>
        </div>
        <ul class="card-list">
          <StartingCard />
          <StartingCard />
          <StartingCard />
          <StartingCard />
        </ul>
      </section>
    </main>
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppJumbo from "./components/AppJumbo.vue";
import StartingCard from "./components/StartingCard.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    AppJumbo,
    StartingCard,
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

#app {
  main {
    width: 80%;
    margin: 0 auto;

    .starting {
      padding: 5rem 0;
      text-align: center;
      .title {
        .secondary-title {
          margin-bottom: 0.5rem;
          color: #959999;
        }

        .primary-title {
          color: #3f3a64;

          h2 {
            font-size: 2.5rem;
          }

          span {
            font-weight: lighter;
            color: #22ad96;
          }
        }
      }
      .card-list {
        display: flex;
        justify-content: space-around;
      }
    }
  }
}
</style>
