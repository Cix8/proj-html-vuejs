<template>
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
        <StartingCard
          v-for="card in staringCardsArray"
          :key="card.image"
          :thisObj="card"
        />
      </ul>
    </section>
    <section class="about-us">
      <div class="top">
        <div class="top_image">
          <div class="img-container">
            <img src="../assets/images/about-us-03-image-01.png" alt="" />
          </div>
          <div class="overlay"></div>
        </div>
        <div class="top_contents">
          <div class="title">
            <div class="secondary-title">
              <span>DREAM WITH MAXCOACH</span>
            </div>
            <div class="primary-title">
              <h2>Construct A <span>STUNNING</span> Career Perspective</h2>
            </div>
          </div>
          <div class="contents-list">
            <ul>
              <li
                v-for="card in aboutUsOptionsArray"
                :key="card.id"
                :class="{ active: currentActive === card.id }"
                @click="
                  currentActive === card.id
                    ? (currentActive = '')
                    : (currentActive = card.id)
                "
              >
                <div class="text">
                  <a>{{ card.title }}</a>
                </div>
                <div class="icon-container">
                  <div
                    class="icon"
                    :class="
                      currentActive === card.id ? 'close-icon' : 'add-icon'
                    "
                  ></div>
                </div>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div class="bottom">
        <ul class="data-list">
          <li v-for="(data, index) in thisCoursesData" :key="index">
            <span>{{ data.number }}</span>
            <strong>{{ data.label }}</strong>
          </li>
        </ul>
      </div>
    </section>
    <section class="featured-courses">
      <div class="title">
        <div class="secondary-title">
          <span>CHOOSE WHERE YOU'D LIKE TO BEGIN</span>
        </div>
        <div class="primary-title">
          <h2>Latest Featured <span>Courses</span></h2>
        </div>
      </div>
      <ul class="courses-list">
        <FeaturedCoursesCard
          v-for="(course, index) in thisFeaturedCourses"
          :key="index"
          :thisCard="course"
        />
      </ul>
      <div class="btn-container">
        <button class="courses-btn">
          <a>View all courses</a>
          <i class="fas fa-long-arrow-alt-right"></i>
        </button>
      </div>
    </section>
  </main>
</template>

<script>
import StartingCard from "./StartingCard.vue";
import FeaturedCoursesCard from "./FeaturedCoursesCard.vue";

export default {
  name: "AppMain",
  components: {
    StartingCard,
    FeaturedCoursesCard,
  },
  props: {
    staringCardsArray: Array,
    aboutUsOptionsArray: Array,
    thisCoursesData: Array,
    thisFeaturedCourses: Array,
  },
  data() {
    return {
      currentActive: 0,
    };
  },
};
</script>

<style lang="scss" scoped>
main {
  width: 80%;
  margin: 0 auto;

  .starting {
    padding-top: 3rem;
    text-align: center;
    .title {
      padding: 2rem;
      .secondary-title {
        margin-bottom: 1.5rem;
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

  .about-us {
    padding-top: 5rem;

    .top {
      height: 650px;
      display: flex;

      &_image {
        position: relative;
        width: 50%;
        height: 100%;

        .img-container {
          position: relative;
          height: 100%;
          z-index: 2;

          img {
            object-fit: contain;
          }
        }

        .overlay {
          position: absolute;
          top: 20%;
          left: -10%;
          width: 70%;
          height: 80%;
          background-image: url("../assets/images/underlay-shape-lilla.svg");
          background-repeat: no-repeat;
          background-size: contain;
        }
      }

      &_contents {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        width: 50%;
        padding: 1rem;
        background-color: #f0efef;

        .title {
          .secondary-title {
            margin-bottom: 1.5rem;
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

        .contents-list {
          ul {
            li {
              display: flex;
              justify-content: space-between;
              align-items: center;
              padding: 0.7rem 1.3rem;
              background-color: #fefefe;
              font-weight: bold;
              cursor: pointer;

              &:not(&:last-child) {
                margin-bottom: 0.7rem;
              }

              &.active {
                border-top-left-radius: 10px;
                border-top-right-radius: 10px;
                background-color: #22ad96;
                color: #fefefe;
              }

              .icon-container {
                width: 30px;
                height: 30px;
                background-color: #959999;

                .icon {
                  width: 100%;
                  height: 100%;

                  &.add-icon {
                    background-color: #fefefe;
                    mask: url("../assets/images/add.svg") no-repeat;
                  }

                  &.close-icon {
                    background-color: #fefefe;
                    mask: url("../assets/images/close.svg") no-repeat center;
                  }
                }
              }
            }
          }
        }
      }
    }

    .bottom {
      padding: 10rem 0;
      .data-list {
        display: flex;
        justify-content: space-around;

        li {
          text-align: center;
          padding: 2rem;
          background-color: #f0efef;

          span {
            display: inline-block;
            margin-bottom: 1rem;
            font-weight: bolder;
            font-size: 2.5rem;
            color: #22ad96;
          }

          strong {
            display: block;
          }
        }
      }
    }
  }

  .featured-courses {
    padding-bottom: 5rem;

    .title {
      text-align: center;
      padding: 2rem;

      .secondary-title {
        margin-bottom: 1.5rem;
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

    .courses-list {
      display: flex;
      flex-wrap: wrap;
      padding-bottom: 3rem;
    }

    .btn-container {
      text-align: center;

      .courses-btn {
        min-width: 20%;
        padding: 1rem 0;
        border: 0;
        border-radius: 5px;
        background-color: #22ad96;
        color: #fefefe;
        vertical-align: middle;
        font-size: 1.1rem;

        i {
          display: inline-block;
          margin-left: 0.8rem;
          vertical-align: middle;
        }

        a {
          vertical-align: middle;
          font-weight: bold;
        }
      }
    }
  }
}
</style>
