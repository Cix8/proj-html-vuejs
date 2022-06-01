<template>
  <footer>
    <div class="footer-contents">
      <div
        class="container"
        v-for="(item, index) in thisFooterData"
        :key="index"
      >
        <div class="title">
          <h4>{{ item.title }}</h4>
        </div>
        <ul
          :class="
            ({ 'address-list': index === 0 }, { 'explore-list': index === 1 })
          "
        >
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
      <span>&copy;2020 Maxcoach, All Rights reserved</span>
    </div>
    <div class="footer-icon">
      <i class="fas fa-arrow-alt-circle-up"></i>
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
footer {
  position: relative;
  .footer-contents {
    position: relative;
    width: 80%;
    margin: 0 auto;
    padding: 5rem 2rem;
    display: flex;
    justify-content: space-between;

    .title {
      margin-bottom: 1rem;
    }

    ul {
      &.explore-list {
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;
        max-height: 100px;

        li {
          margin: 0 4rem 0.5rem 0;
        }
      }

      li {
        margin-bottom: 0.5rem;
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
    padding: 3rem;
    text-align: center;
    color: #959999;
  }

  .footer-icon {
    position: absolute;
    bottom: 0;
    right: 0;
    font-size: 3rem;
    margin: 1.5rem;
    color: #22ad96;
  }
}
</style>
