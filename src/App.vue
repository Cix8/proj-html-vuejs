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
          <StartingCard
            v-for="card in startingCards"
            :key="card.image"
            :thisObj="card"
          />
        </ul>
      </section>
      <section class="about-us">
        <div class="top">
          <div class="top_image">
            <div class="img-container">
              <img src="./assets/images/about-us-03-image-01.png" alt="" />
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
                <li class="active">
                  <div class="text">
                    <a
                      >Multiple Platforms Supported for Teaching &amp;
                      Studing</a
                    >
                  </div>
                  <div class="icon-container">
                    <div class="icon close-icon"></div>
                  </div>
                </li>
                <li>
                  <div class="text">
                    <a
                      >Multiple Platforms Supported for Teaching &amp;
                      Studing</a
                    >
                  </div>
                  <div class="icon-container">
                    <div class="icon add-icon"></div>
                  </div>
                </li>
                <li>
                  <div class="text">
                    <a
                      >Multiple Platforms Supported for Teaching &amp;
                      Studing</a
                    >
                  </div>
                  <div class="icon-container">
                    <div class="icon add-icon"></div>
                  </div>
                </li>
              </ul>
            </div>
          </div>
        </div>
        <div class="bottom">
          <ul class="data-list">
            <li>
              <span>1.926</span>
              <strong>FINISHED SESSIONS</strong>
            </li>
            <li>
              <span>1.926</span>
              <strong>FINISHED SESSIONS</strong>
            </li>
            <li>
              <span>1.926</span>
              <strong>FINISHED SESSIONS</strong>
            </li>
            <li>
              <span>1.926</span>
              <strong>FINISHED SESSIONS</strong>
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
          <li>
            <div class="card-img">
              <img src="./assets/images/stock-full-hd-03-480x298.jpg" alt="" />
              <div class="price">
                <span>$26.00</span>
              </div>
            </div>
            <div class="card-data">
              <div class="profile">
                <div class="profile-icon">
                  <img
                    src="./assets/images/73ee246daf47502812ccefc84bf02898.jpeg"
                    alt=""
                  />
                </div>
                <div class="profile-name">
                  <span>Blanche Fields</span>
                </div>
              </div>
              <div class="card-title">
                <h3>Leaning to Write as a Professional Author</h3>
              </div>
            </div>
            <div class="card-info">
              <div class="container">
                <i class="far fa-clipboard"></i>
                <span>20 Lessons</span>
              </div>
              <div class="container">
                <i class="far fa-user"></i>
                <span>50 Students</span>
              </div>
            </div>
          </li>
          <li>
            <div class="card-img">
              <img src="./assets/images/stock-full-hd-03-480x298.jpg" alt="" />
              <div class="price">
                <span>Free</span>
              </div>
            </div>
            <div class="card-data">
              <div class="profile">
                <div class="profile-icon">
                  <img
                    src="./assets/images/73ee246daf47502812ccefc84bf02898.jpeg"
                    alt=""
                  />
                </div>
                <div class="profile-name">
                  <span>Blanche Fields</span>
                </div>
              </div>
              <div class="card-title">
                <h3>Leaning to Write as a Professional Author</h3>
              </div>
            </div>
            <div class="card-info">
              <div class="container">
                <i class="far fa-clipboard"></i>
                <span>20 Lessons</span>
              </div>
              <div class="container">
                <i class="far fa-user"></i>
                <span>50 Students</span>
              </div>
            </div>
          </li>
          <li>
            <div class="card-img">
              <img src="./assets/images/stock-full-hd-03-480x298.jpg" alt="" />
              <div class="price">
                <span>$26.00</span>
              </div>
            </div>
            <div class="card-data">
              <div class="profile">
                <div class="profile-icon">
                  <img
                    src="./assets/images/73ee246daf47502812ccefc84bf02898.jpeg"
                    alt=""
                  />
                </div>
                <div class="profile-name">
                  <span>Blanche Fields</span>
                </div>
              </div>
              <div class="card-title">
                <h3>Leaning to Write as a Professional Author</h3>
              </div>
            </div>
            <div class="card-info">
              <div class="container">
                <i class="far fa-clipboard"></i>
                <span>20 Lessons</span>
              </div>
              <div class="container">
                <i class="far fa-user"></i>
                <span>50 Students</span>
              </div>
            </div>
          </li>
          <li>
            <div class="card-img">
              <img src="./assets/images/stock-full-hd-03-480x298.jpg" alt="" />
              <div class="price">
                <span>$26.00</span>
              </div>
            </div>
            <div class="card-data">
              <div class="profile">
                <div class="profile-icon">
                  <img
                    src="./assets/images/73ee246daf47502812ccefc84bf02898.jpeg"
                    alt=""
                  />
                </div>
                <div class="profile-name">
                  <span>Blanche Fields</span>
                </div>
              </div>
              <div class="card-title">
                <h3>Leaning to Write as a Professional Author</h3>
              </div>
            </div>
            <div class="card-info">
              <div class="container">
                <i class="far fa-clipboard"></i>
                <span>20 Lessons</span>
              </div>
              <div class="container">
                <i class="far fa-user"></i>
                <span>50 Students</span>
              </div>
            </div>
          </li>
          <li>
            <div class="card-img">
              <img src="./assets/images/stock-full-hd-03-480x298.jpg" alt="" />
              <div class="price">
                <span>$26.00</span>
              </div>
            </div>
            <div class="card-data">
              <div class="profile">
                <div class="profile-icon">
                  <img
                    src="./assets/images/73ee246daf47502812ccefc84bf02898.jpeg"
                    alt=""
                  />
                </div>
                <div class="profile-name">
                  <span>Blanche Fields</span>
                </div>
              </div>
              <div class="card-title">
                <h3>Leaning to Write as a Professional Author</h3>
              </div>
            </div>
            <div class="card-info">
              <div class="container">
                <i class="far fa-clipboard"></i>
                <span>20 Lessons</span>
              </div>
              <div class="container">
                <i class="far fa-user"></i>
                <span>50 Students</span>
              </div>
            </div>
          </li>
          <li>
            <div class="card-img">
              <img src="./assets/images/stock-full-hd-03-480x298.jpg" alt="" />
              <div class="price">
                <span>$26.00</span>
              </div>
            </div>
            <div class="card-data">
              <div class="profile">
                <div class="profile-icon">
                  <img
                    src="./assets/images/73ee246daf47502812ccefc84bf02898.jpeg"
                    alt=""
                  />
                </div>
                <div class="profile-name">
                  <span>Blanche Fields</span>
                </div>
              </div>
              <div class="card-title">
                <h3>Leaning to Write as a Professional Author</h3>
              </div>
            </div>
            <div class="card-info">
              <div class="container">
                <i class="far fa-clipboard"></i>
                <span>20 Lessons</span>
              </div>
              <div class="container">
                <i class="far fa-user"></i>
                <span>50 Students</span>
              </div>
            </div>
          </li>
        </ul>
        <div class="btn-container">
          <button class="courses-btn">
            <a>View all courses</a>
            <i class="fas fa-long-arrow-alt-right"></i>
          </button>
        </div>
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
      startingCards: [
        {
          image: "01",
          title: "Idea Discussion",
          text: "Get teamed up with the specialists who work and teach coding for years at famous university",
        },
        {
          image: "02",
          title: "Web Development",
          text: "Learn to start building a webpage from scratch. You decide your own pace, course and speed",
        },
        {
          image: "03",
          title: "System Administration",
          text: "Learners are encouraged to study the mechanism and structure of system administration",
        },
        {
          image: "04",
          title: "Graphic Design",
          text: "Have a passion for graphic and arts? Show your talents with confidence and self-assertiveness",
        },
      ],
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
            background-image: url("./assets/images/underlay-shape-lilla.svg");
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

                &:not(&:last-child) {
                  margin-bottom: 0.7rem;
                }

                &.active {
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
                      mask: url("./assets/images/add.svg") no-repeat;
                    }

                    &.close-icon {
                      background-color: #fefefe;
                      mask: url("./assets/images/close.svg") no-repeat center;
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

        li {
          position: relative;
          width: calc(100% / 3);
          padding: 2.5rem;

          .card-img {
            position: relative;
            margin-bottom: 1rem;
            border-top-left-radius: 20px;
            border-top-right-radius: 20px;
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

          .card-data {
            width: 70%;

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
}
</style>
