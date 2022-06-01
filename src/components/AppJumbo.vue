<template>
  <div class="jumbo">
    <div class="jumbo_overlay"></div>
    <div class="general-container">
      <div class="left-col">
        <div class="text">
          <h2>Complete Your Dreams in JavaS Programming</h2>
          <span>
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Doloremque
            minus necessitatibus, sint at repellat tempora aut commodi eius.
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
  word-break: break-all;
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
    width: 75%;
    margin: 0 auto;
    padding: 2rem 0;
    display: flex;
    align-items: center;

    .left-col,
    .right-col {
      width: 50%;
      height: 100%;
    }

    .text {
      width: 85%;
      padding-right: 3rem;
      margin-bottom: 1.5rem;
      font-size: 1.6rem;

      h2 {
        margin-bottom: 1.5rem;
      }
      span {
        font-size: 1.2rem;
        line-height: 2.8rem;
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
</style>
