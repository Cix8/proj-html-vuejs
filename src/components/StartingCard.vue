<template>
  <li>
    <div class="card-image">
      <img
        :src="
          require('../assets/images/home-5-image-box-' + thisObj.image + '.png')
        "
        :alt="thisObj.title"
      />
    </div>
    <div class="card-title">
      <h3>{{ thisObj.title }}</h3>
    </div>
    <div class="card-text">
      <span>{{ thisObj.text }}</span>
    </div>
    <div class="card-link">
      <a
        >Start now <span><i class="fas fa-long-arrow-alt-right"></i></span
      ></a>
    </div>
  </li>
</template>

<script>
export default {
  name: "StartingCard",
  props: {
    thisObj: Object,
  },
};
</script>

<style lang="scss" scoped>
li {
  padding: 0 1rem;
  .card-image {
    width: 200px;
    height: 200px;
    margin: 2.5rem auto;

    img {
      object-fit: contain;
    }
  }
  .card-title {
    margin-bottom: 1rem;
  }

  .card-text {
    color: #959999;
    line-height: 1.5rem;
    margin-bottom: 1.5rem;
  }

  .card-link {
    color: #96a6a5;
    font-weight: bold;

    a {
      cursor: pointer;

      span {
        display: inline-block;
        margin-left: 0.5rem;
      }
    }

    a:hover {
      color: #22ad96;
    }
  }
}
</style>
