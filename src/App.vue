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
        <div class="about-us_image">
          <div class="img-container">
            <img src="./assets/images/about-us-03-image-01.png" alt="" />
          </div>
          <div class="overlay"></div>
        </div>
        <div class="contents">
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
                  <a>Multiple Platforms Supported for Teaching &amp; Studing</a>
                </div>
                <div class="icon-container">
                  <div class="icon close-icon"></div>
                </div>
              </li>
              <li>
                <div class="text">
                  <a>Multiple Platforms Supported for Teaching &amp; Studing</a>
                </div>
                <div class="icon-container">
                  <div class="icon add-icon"></div>
                </div>
              </li>
              <li>
                <div class="text">
                  <a>Multiple Platforms Supported for Teaching &amp; Studing</a>
                </div>
                <div class="icon-container">
                  <div class="icon add-icon"></div>
                </div>
              </li>
            </ul>
          </div>
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
    padding-bottom: 5rem;
    width: 80%;
    margin: 0 auto;

    .starting {
      padding-top: 5rem;
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

    .about-us {
      padding-top: 5rem;
      height: 500px;
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
          background-color: #b6b8d1;
          mask: url("./assets/images/underlay-shape-grey.svg") no-repeat;
          mask-size: contain;
        }
      }

      .contents {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        width: 50%;
        padding: 1rem;
        background-color: #f0efef;

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

        &-list {
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
  }
}
</style>
