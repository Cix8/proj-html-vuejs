<template>
  <footer>
    <div class="footer-contents">
      <div
        class="container"
        v-for="(item, index) in thisFooterData"
        :key="index"
        :class="item.title.toLowerCase()"
      >
        <div class="title">
          <h4>{{ item.title }}</h4>
        </div>
        <ul :class="item.title.toLowerCase() + '-list'">
          <li v-for="(link, anotherIndex) in item.links" :key="anotherIndex">
            <a>{{ link }}</a>
          </li>
        </ul>
      </div>
      <div class="social">
        <ul>
          <li v-for="(social, index) in theseSocial" :key="index">
            <i :class="'fab fa-' + social"></i>
          </li>
        </ul>
      </div>
    </div>
    <div class="credits">
      <div class="text">
        <span>&copy;2020 Maxcoach, All Rights reserved</span>
      </div>
      <div class="footer-icon">
        <i class="fas fa-arrow-alt-circle-up"></i>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "AppFooter",
  props: {
    thisFooterData: Array,
    theseSocial: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

footer {
  .footer-contents {
    position: relative;
    width: $generalWidth;
    margin: 0 auto;
    padding: 5rem 2rem 3rem;
    display: flex;

    .container {
      &.address {
        min-width: 50%;
      }

      .title {
        margin-bottom: 1.5rem;
      }

      ul {
        &.explore-list {
          min-width: 300px;
          max-height: 130px;
          display: flex;
          flex-direction: column;
          flex-wrap: wrap;

          li {
            margin: 0 4rem 1rem 0;
          }
        }

        li {
          color: #959999;
          margin-bottom: 1rem;
        }
      }
    }

    .social {
      position: absolute;
      bottom: 2rem;
      left: 2rem;
      width: 200px;

      ul {
        display: flex;
        justify-content: space-between;
        font-size: 1.8rem;
        color: #959999;
      }
    }
  }

  .credits {
    position: relative;
    padding: 3rem;
    color: #959999;

    .text {
      text-align: center;
    }

    .footer-icon {
      position: absolute;
      top: 0;
      right: 0;
      font-size: 3rem;
      margin: 2rem;
      color: #22ad96;
    }
  }
}
</style>
