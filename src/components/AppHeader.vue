<template>
  <header>
    <div class="general-container">
      <div class="logo-container">
        <img src="../assets/images/dark-logo.png" alt="" />
      </div>
      <nav>
        <ul class="col-left">
          <li v-for="(link, index) in linksArray" :key="index">
            <a>{{ link }}</a>
            <div class="chevron">
              <i class="fas fa-chevron-down"></i>
            </div>
          </li>
        </ul>
        <div class="col-right">
          <ul class="icons-container">
            <li class="cart">
              <i class="fas fa-shopping-cart"></i>
              <div class="cart-items">
                <small>{{ theseCartItems.length }}</small>
              </div>
            </li>
            <li class="profile"><i class="far fa-user-circle"></i></li>
          </ul>
          <div class="search-container">
            <div class="input-container">
              <input type="text" id="search-input" placeholder="Search..." />
            </div>
            <div class="search-icon">
              <i class="fas fa-search"></i>
            </div>
          </div>
        </div>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
  props: {
    linksArray: Array,
    theseCartItems: Array,
  },
};
</script>

<style lang="scss" scoped>
header {
  padding: 1.5rem 0;
  background-color: #f0efef;

  .general-container {
    width: 80%;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;

    .logo-container {
      width: 200px;
    }

    nav {
      width: calc(100% - 200px);
      display: flex;

      .col-left {
        width: 65%;
        display: flex;
        justify-content: flex-end;
        align-items: center;

        li {
          display: flex;

          &:not(&:first-child) {
            margin-left: 1.5rem;
          }

          .chevron {
            margin-left: 0.3rem;
          }
        }
      }

      .col-right {
        width: 35%;
        display: flex;
        justify-content: space-between;
        align-items: center;

        .icons-container {
          display: flex;
          justify-content: space-between;
          flex-grow: 1;
          padding: 0 1rem;
          font-size: 1.1rem;

          li {
            &:first-child {
              align-self: flex-end;
            }

            &.cart {
              position: relative;

              .cart-items {
                position: absolute;
                top: -25%;
                right: -10%;
                transform: translate(+50%, -50%);
                padding: 0 0.4rem;
                border-radius: 50%;
                background-color: #22ad96;
                font-weight: bold;
                color: #fefefe;
              }
            }
          }
        }

        .search-container {
          justify-self: flex-end;
          display: flex;
          align-items: center;
          border: 1px solid transparent;

          &:focus-within {
            border: 1px solid #01aa51;
          }

          .input-container input {
            width: 150px;
          }

          .input-container input:focus-visible {
            outline: 0;
          }

          .input-container input,
          .search-icon i {
            border: 0;
            padding: 0.7rem 1rem;
          }

          .search-icon {
            background-color: #fefefe;
            color: #01aa51;
          }
        }
      }
    }
  }
}
</style>
