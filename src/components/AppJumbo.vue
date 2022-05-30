<template>
  <div class="jumbo">
    <div class="jumbo_overlay"></div>
    <div class="general-container">
      <div class="left-col">
        <div class="text">
          <h2>Complete Your Dreams in JavaS Programming</h2>
          <small>
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Doloremque
            minus necessitatibus, sint at repellat tempora aut commodi eius.
          </small>
        </div>
        <div class="btn-container">
          <button>
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
    width: 80%;
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
      padding-right: 3rem;
      margin-bottom: 1.5rem;
      font-size: 1.8rem;
      h2 {
        width: 85%;
        margin-bottom: 1.5rem;
      }
      small {
        line-height: 2.8rem;
      }
    }

    .btn-container {
      button {
        min-width: 40%;
        padding: 1rem 0;
        border: 0;
        border-radius: 10px;
        background-color: #22ad96;
        color: #fefefe;
        vertical-align: middle;

        i {
          font-size: 1.2rem;
          vertical-align: middle;
        }

        a {
          display: inline-block;
          margin-left: 0.8rem;
          font-weight: bold;
          font-size: 0.9rem;
        }
      }
    }
  }
}
</style>
