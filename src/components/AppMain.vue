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
              <span>DREAM WITH <strong>MAXCOACH</strong></span>
            </div>
            <div class="primary-title">
              <h2>Construct A <span>Stunning</span> Career Perspective</h2>
            </div>
          </div>
          <div class="contents-list">
            <ul>
              <li
                v-for="option in aboutUsOptionsArray"
                :key="option.id"
                :class="{ active: currentActive === option.id }"
                @click="
                  currentActive === option.id
                    ? (currentActive = '')
                    : (currentActive = option.id)
                "
              >
                <div class="option-top">
                  <div class="text">
                    <a>{{ option.title }}</a>
                  </div>
                  <div
                    class="icon-container"
                    :class="{ active: currentActive === option.id }"
                  >
                    <div
                      class="icon"
                      :class="
                        currentActive === option.id ? 'close-icon' : 'add-icon'
                      "
                    ></div>
                  </div>
                </div>
                <template v-if="currentActive === option.id">
                  <div class="option-bottom">
                    <p>{{ option.content }}</p>
                  </div>
                </template>
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
        <button class="green-btn">
          <a>View all courses</a>
          <i class="fas fa-long-arrow-alt-right"></i>
        </button>
      </div>
    </section>
    <section class="main-banner">
      <div class="col-left">
        <div class="title">
          <div class="secondary-title">
            <span>WHY ESITATE TO REGISTER?</span>
          </div>
          <div class="primary-title">
            <h2>Learn At Your Own <span>Pace</span></h2>
          </div>
        </div>
        <div class="options">
          <ul class="options-list fa-ul">
            <li>
              <span class="fa-li"><i class="fas fa-check"></i></span> Select &
              customize courses to your preferences
            </li>
            <li>
              <span class="fa-li"><i class="fas fa-check"></i></span>Change the
              tutor and make arrangements
            </li>
            <li>
              <span class="fa-li"><i class="fas fa-check"></i></span>Patercipate
              in events to join others
            </li>
            <li>
              <span class="fa-li"><i class="fas fa-check"></i></span>Get the
              desired certificate delivered at the house
            </li>
          </ul>
          <div class="btn-container">
            <button class="green-btn">
              <a>Get started for Free</a>
            </button>
          </div>
        </div>
      </div>
      <div class="col-right">
        <div class="img-container">
          <img src="../assets/images/home-5-image-01.png" alt="" />
        </div>
      </div>
    </section>
    <section class="main-banner reverse">
      <div class="col-left">
        <div class="title">
          <div class="secondary-title">
            <span>WHAT ARE YOU LOOKING FOR?</span>
          </div>
          <div class="primary-title">
            <h2>Learn on your <span>Mobile</span> anytime!</h2>
          </div>
        </div>
        <div class="text">
          <p>
            Save lessons for later and revise or write notes at any time and on
            multiple devices on your way. Never interfere with activities of
            enjoyment or other precious moments.
          </p>
        </div>
        <div class="btn-container">
          <button class="green-btn">
            <a>Download Our App</a>
          </button>
        </div>
      </div>
      <div class="col-right">
        <div class="img-container">
          <img src="../assets/images/home-5-image-02.png" alt="" />
        </div>
      </div>
    </section>
    <section class="events">
      <div class="top">
        <div class="title">
          <div class="secondary-title">
            <span>GET IN CONTACT NOW</span>
          </div>
          <div class="primary-title">
            <h2>Upcoming <span>Events</span></h2>
          </div>
        </div>
      </div>
      <div class="contents">
        <ul class="contents-list">
          <AppEvent
            v-for="(event, index) in thisEventsArray"
            :key="index"
            :thisEvent="event"
          />
        </ul>
      </div>
      <div class="bottom">
        <span
          >Exicted about our events?
          <a>View all events <i class="fas fa-long-arrow-alt-right"></i></a
        ></span>
      </div>
    </section>
    <section class="testimonials">
      <div class="top">
        <div class="title">
          <div class="secondary-title">
            <span>PEOPLE ARE PRAISING MAXCOACH</span>
          </div>
          <div class="primary-title">
            <h2>What make they <span>love us?</span></h2>
          </div>
        </div>
      </div>
      <div class="contents">
        <ul class="contents-list">
          <li
            v-for="testimonial in thisTestimonialsArray[currentTestimonials]"
            :key="testimonial.image"
          >
            <div class="container">
              <div class="top">
                <img
                  :src="
                    require('../assets/images/testimonial-avata-' +
                      testimonial.image +
                      '.jpg')
                  "
                  alt=""
                />
              </div>
              <div class="bottom">
                <p>
                  {{ testimonial.text }}
                </p>
                <strong>{{ testimonial.name.toUpperCase() }}</strong>
                <span>/ {{ testimonial.occupation }}</span>
              </div>
            </div>
          </li>
        </ul>
        <ul class="circles-list">
          <li
            v-for="(element, index) in thisTestimonialsArray"
            :key="index"
            :class="{ active: currentTestimonials === index }"
            @click="currentTestimonials = index"
          >
            <i class="fas fa-circle"></i>
          </li>
        </ul>
      </div>
    </section>
    <section class="small-banner">
      <div class="small-banner_title">
        <div class="secondary-title">
          <h3>Start today for getting <span>Online Certification</span></h3>
        </div>
        <div class="primary-title">
          <h2>You can be your own guiding star with our help!</h2>
        </div>
      </div>
      <div class="btn-container">
        <div class="btn-container">
          <button class="green-btn">
            <a>Get started now</a>
          </button>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import StartingCard from "./StartingCard.vue";
import FeaturedCoursesCard from "./FeaturedCoursesCard.vue";
import AppEvent from "./AppEvent.vue";

export default {
  name: "AppMain",
  components: {
    StartingCard,
    FeaturedCoursesCard,
    AppEvent,
  },
  props: {
    staringCardsArray: Array,
    aboutUsOptionsArray: Array,
    thisCoursesData: Array,
    thisFeaturedCourses: Array,
    thisEventsArray: Array,
    thisTestimonialsArray: Array,
  },
  data() {
    return {
      currentActive: 0,
      currentTestimonials: 0,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

main {
  width: $generalWidth;
  margin: 0 auto;

  .starting {
    padding-top: 3rem;
    text-align: center;

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
        height: 90%;

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
          padding: 0;
        }

        .contents-list {
          ul {
            li {
              font-weight: bold;
              cursor: pointer;

              &:not(&:last-child) {
                margin-bottom: 0.7rem;
              }

              &.active {
                .option-top {
                  border-top-left-radius: 10px;
                  border-top-right-radius: 10px;
                  background-color: #22ad96;
                  color: #fefefe;
                }
              }

              .option-top {
                display: flex;
                justify-content: space-between;
                align-items: center;
                padding: 0.7rem 1.3rem;
                background-color: #fefefe;

                .icon-container {
                  width: 30px;
                  height: 30px;
                  border-radius: 50%;
                  flex-shrink: 0;
                  background-color: #959999;

                  &.active {
                    background-color: #fefefe;
                  }

                  .icon {
                    width: 100%;
                    height: 100%;

                    &.add-icon {
                      background-color: #fefefe;
                      mask: url("../assets/images/add.svg") no-repeat;
                    }

                    &.close-icon {
                      position: relative;

                      &::before {
                        font: var(--fa-font-solid);
                        content: "\f068";
                        position: absolute;
                        top: 50%;
                        left: 50%;
                        transform: translate(-50%, -50%);
                        color: #22ad96;
                        font-size: 1.2rem;
                      }
                    }
                  }
                }
              }

              .option-bottom {
                padding: 2rem 1rem;
                font-size: 0.9rem;
                background-color: #f0efef;

                p {
                  padding: 1rem;
                  background-color: #fefefe;
                  color: #3f3a64;
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
    }

    .courses-list {
      display: flex;
      flex-wrap: wrap;
      padding-bottom: 3rem;
    }

    .btn-container {
      text-align: center;

      .green-btn {
        min-width: 20%;

        i {
          display: inline-block;
          margin-left: 0.8rem;
          vertical-align: middle;
        }

        a {
          vertical-align: middle;
        }
      }
    }
  }

  .main-banner {
    position: relative;
    min-height: 500px;
    display: flex;
    padding-top: 5rem;

    &::before {
      content: "";
      position: absolute;
      top: 35%;
      right: 20%;
      width: $shapeGreySize;
      height: $shapeGreySize;
      background-image: url("../assets/images/underlay-shape-grey.svg");
      background-size: cover;
    }

    &::after {
      content: "";
      position: absolute;
      top: 55%;
      right: 0;
      background-image: url("../assets/images/maxcoach-shape-05.png");
      background-repeat: no-repeat;
      background-size: cover;
      width: $shapeBulletedSize;
      height: $shapeBulletedSize;
    }

    &:not(&.reverse) {
      .col-left {
        .title {
          max-width: 80%;
          padding: 2rem 2rem 1rem;
        }
      }
    }

    .col-left {
      width: 40%;

      .options {
        padding: 1rem;

        .options-list {
          li {
            margin-bottom: 1.5rem;

            span {
              font-size: 1.2rem;
              color: #22ad96;
            }
          }
        }

        .btn-container {
          padding: 1rem 0.6rem 0;

          .green-btn {
            min-width: 55%;
          }
        }
      }
    }

    .col-right {
      width: 60%;

      .img-container {
        position: relative;
        z-index: 2;
        width: 60%;
        margin: 0 auto;
        padding: 2rem 0;
      }
    }

    &.reverse {
      flex-direction: row-reverse;
      align-items: center;

      &::before {
        top: 30%;
        right: 0;
        left: 2%;
      }

      &::after {
        top: 60%;
        right: 0;
        left: 35%;
        width: $shapeSquareBulletedSize;
        height: $shapeSquareBulletedSize;
        background-image: url("../assets/images/maxcoach-shape-07.png");
      }

      .col-left {
        .title {
          padding: 1rem 0;
        }

        .text {
          margin-bottom: 2rem;

          p {
            line-height: 30px;
          }
        }

        .btn-container {
          padding: 1rem 0;

          .green-btn {
            min-width: 50%;
          }
        }
      }

      .col-right {
        &::before {
          content: "";
          position: absolute;
          top: 55%;
          left: -5%;
          width: $shapeStairsSize;
          height: $shapeStairsSize;
          background-image: url("../assets/images/maxcoach-shape-01.png");
          background-repeat: no-repeat;
          background-size: contain;
        }

        &::after {
          content: "";
          position: absolute;
          top: 30%;
          left: 45%;
          width: 50px;
          height: 50px;
          transform: translateX(-50%);
          border: 10px solid #de912a;
          border-radius: 50%;
          opacity: 0.5;
        }

        .img-container {
          img {
            width: 80%;
          }
        }
      }
    }
  }

  .events {
    .top {
      .title {
        padding: 5rem;
        text-align: center;
      }
    }

    .contents {
      &-list {
        display: flex;
        flex-wrap: wrap;
      }
    }

    .bottom {
      padding: 5rem;
      text-align: center;
      font-size: 1.1rem;
      color: #959999;

      a {
        font-weight: bold;
        cursor: pointer;

        &:hover {
          color: #22ad96;
        }
      }
    }
  }

  .testimonials {
    .top {
      .title {
        padding: 10rem 0 8rem;
        text-align: center;
      }
    }

    .contents {
      &-list {
        display: flex;

        li {
          max-width: calc(100% / 3);
          padding: 2rem;

          .container {
            position: relative;
            min-height: 330px;
            padding: 0 1rem 2rem;
            text-align: center;
            box-shadow: 10px 10px 50px #959999;

            .top {
              position: absolute;
              top: 0;
              left: 50%;
              transform: translate(-50%, -50%);
              width: 40%;

              img {
                border-radius: 50%;
              }
            }

            .bottom {
              padding: 8rem 0 0;

              p {
                width: 90%;
                margin: 0 auto 2rem;
              }

              strong {
                display: block;
                margin-bottom: 0.5rem;
                font-size: 0.9rem;
              }

              span {
                font-size: 0.9rem;
                color: #959999;
              }
            }
          }
        }
      }

      .circles-list {
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 3rem 5rem 5rem;

        li {
          display: flex;
          margin: 0 0.5rem;
          font-size: 0.6rem;
          color: #959999;
          cursor: pointer;

          &.active {
            font-size: 1rem;
            color: #000000;
          }
        }
      }
    }
  }

  .small-banner {
    position: relative;
    padding: 2rem 2rem 5rem;
    text-align: center;
    color: #3f3a64;

    &::before {
      content: "";
      position: absolute;
      top: 40%;
      left: 5%;
      width: $shapeStairsSize;
      height: $shapeStairsSize;
      background-image: url("../assets/images/maxcoach-shape-01.png");
      background-repeat: no-repeat;
      background-size: contain;
    }

    &::after {
      content: "";
      position: absolute;
      top: 0;
      left: 5%;
      width: 50px;
      height: 50px;
      transform: translateX(-50%);
      border: 10px solid #de912a;
      border-radius: 50%;
      opacity: 0.3;
    }

    &_title {
      &::after {
        content: "";
        position: absolute;
        top: 40%;
        right: 3%;
        width: 120px;
        height: 120px;
        background-image: url("../assets/images/maxcoach-shape-02.png");
        background-repeat: no-repeat;
        background-size: contain;
      }
      .secondary-title {
        font-size: 1.2rem;
        margin-bottom: 0.5rem;

        span {
          font-weight: lighter;
          font-size: 1.3rem;
          color: #22ad96;
        }
      }

      .primary-title {
        margin-bottom: 2rem;
        font-size: 1.4rem;
      }
    }

    .btn-container {
      text-align: center;

      .green-btn {
        min-width: 25%;
      }
    }
  }
}
</style>
