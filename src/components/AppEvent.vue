<template>
  <li>
    <div class="container">
      <div class="col-left">
        <span>
          <i class="fas fa-map-marker-alt"></i>
          {{ thisEvent.location }}
        </span>
        <h3>{{ thisEvent.title }}</h3>
      </div>
      <div class="col-right">
        <div class="date">
          <span class="day">{{ thisEvent.date.day }}</span>
          <span class="month">{{
            thisEvent.date.month.slice(0, 3).toUpperCase()
          }}</span>
        </div>
        <div class="btn-container">
          <button class="green-btn">
            <a>Get Ticket</a>
          </button>
        </div>
      </div>
    </div>
  </li>
</template>

<script>
export default {
  name: "AppEvent",
  props: {
    thisEvent: Object,
  },
};
</script>

<style lang="scss" scoped>
li {
  width: 50%;
  padding: 1rem;

  &:hover {
    .container {
      border-left-color: #01aa51;
    }

    .btn-container {
      .green-btn {
        background-color: #513e5e;
      }
    }
  }

  .container {
    display: flex;
    justify-content: space-between;
    padding: 1rem;
    border-left: 3px solid transparent;
    border-top-left-radius: 10px;
    border-bottom-left-radius: 10px;
    background-color: #f0efef;

    .col-left {
      max-width: 70%;
      padding: 1rem;

      span {
        display: inline-block;
        margin-bottom: 1rem;
        color: #959999;
      }
    }

    .col-right {
      .date {
        text-align: center;

        span.day {
          display: block;
          font-size: 3rem;
          color: #01aa51;
        }

        span.month {
          display: block;
          padding-bottom: 0.5rem;
          font-weight: bold;
        }
      }

      .btn-container {
        text-align: center;

        .green-btn {
          padding: 0.5rem 2.5rem;
          font-size: 0.9rem;

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
  }
}
</style>
