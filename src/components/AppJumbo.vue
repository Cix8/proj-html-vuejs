<template>
  <div class="jumbo">
    <div class="jumbo_overlay"></div>
    <div class="general-container">
      <div class="left-col">
        <div class="text">
          <h2>
            Complete Your <span>Dreams</span> in <span>JavaS</span> Programming
          </h2>
          <span>
            Learn any coding program in distance and for a reasonable fee. You
            don't have to struggle alone, you've got our assistance and help
          </span>
        </div>
        <div class="btn-container">
          <button class="green-btn">
            <i class="fas fa-download"></i>
            <a>Download free E-book</a>
          </button>
        </div>
      </div>
      <div class="right-col">
        <img src="../assets/images/home-5-hero-image.png" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppJumbo",
};
</script>

<style lang="scss" scoped>
.jumbo {
  position: relative;
  min-height: 500px;
  background-color: #f0efef;
  color: #3f3a64;

  &_overlay {
    position: absolute;
    top: 40%;
    left: 0;
    width: 100%;
    height: 60%;
    background-image: url("../assets/images/jumbo-overlay.svg");
    transform: rotateX(180deg);
    z-index: 0;
  }

  .general-container {
    position: relative;
    z-index: 2;
    width: 80%;
    margin: 0 auto;
    padding: 3rem 0;
    display: flex;

    .left-col,
    .right-col {
      width: 50%;
      height: 100%;
    }

    .left-col {
      padding: 4rem 0 0;
      .text {
        width: 85%;
        margin-bottom: 2rem;
        font-size: 1.9rem;

        h2 {
          max-width: 80%;
          margin-bottom: 1.5rem;

          span {
            font-size: inherit;
            word-break: keep-all;
          }
        }
        span {
          display: inline-block;
          max-width: 90%;
          font-size: 1.3rem;
          line-height: 2.5rem;
        }
      }

      .btn-container {
        .green-btn {
          min-width: 50%;

          i {
            vertical-align: middle;
          }

          a {
            display: inline-block;
            margin-left: 0.8rem;
            vertical-align: middle;
          }
        }
      }
    }
  }
}
</style>
