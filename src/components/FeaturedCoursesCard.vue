<template>
  <li>
    <div class="card-img">
      <img
        :src="
          thisCard.image[0] !== 'h'
            ? require('../assets/images/course-' +
                thisCard.image +
                '-480x298.jpg')
            : require('../assets/images/stock-full-' +
                thisCard.image +
                '-480x298.jpg')
        "
        :alt="thisCard.name"
      />
      <div class="price">
        <template v-if="isNaN(thisCard.price[0])">
          <span>{{ thisCard.price }}</span>
        </template>
        <template v-else>
          <span>{{ "$" + thisCard.price.split(".")[0] }}.</span>
          <small>{{ thisCard.price.split(".")[1] }}</small>
        </template>
      </div>
    </div>
    <div class="card-text">
      <div class="card-data">
        <div class="profile">
          <div class="profile-icon">
            <img
              :src="require('../assets/images/' + thisCard.avatar + '.jpeg')"
              :alt="thisCard.name"
            />
          </div>
          <div class="profile-name">
            <span>{{ thisCard.name }}</span>
          </div>
        </div>
        <div class="card-title">
          <h3>{{ thisCard.text }}</h3>
        </div>
      </div>
      <div class="card-info">
        <div class="container">
          <i class="far fa-clipboard"></i>
          <span>{{ thisCard.statics.lessons + " Lessons" }}</span>
        </div>
        <div class="container">
          <i class="far fa-user"></i>
          <span>{{ thisCard.statics.students + " Students" }}</span>
        </div>
      </div>
    </div>
  </li>
</template>

<script>
export default {
  name: "FeaturedCoursesCard",
  props: {
    thisCard: Object,
  },
};
</script>

<style lang="scss" scoped>
li {
  position: relative;
  width: calc(100% / 3);
  padding: 2.5rem;
  cursor: pointer;

  &:hover {
    box-shadow: 10px 10px 50px #959999;

    .card-img,
    .card-text {
      background-color: #fefefe;
    }
  }

  .card-img {
    position: relative;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
    overflow: hidden;

    .price {
      position: absolute;
      top: 0;
      right: 0;
      padding: 0.5rem 1rem;
      border-bottom-left-radius: 10px;
      background-color: #22ad96;
      font-weight: bold;
      color: #fefefe;
    }
  }

  .card-text {
    padding: 1rem 0;

    .card-data {
      width: 90%;

      .profile {
        display: flex;
        align-items: center;

        &-icon {
          width: 32px;
          margin: 0.5rem;
          border-radius: 50%;
          overflow: hidden;
        }

        &-name {
          color: #959999;
        }
      }

      .card-title {
        padding: 0.5rem 0.7rem 2rem;
      }
    }

    .card-info {
      display: flex;
      padding-left: 0.7rem;
      color: #959999;

      .container {
        margin-right: 1rem;

        span {
          display: inline-block;
          margin-left: 0.5rem;
          font-size: 0.8rem;
          vertical-align: middle;
        }
      }
    }
  }
}
</style>
