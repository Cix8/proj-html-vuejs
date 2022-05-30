<template>
  <li>
    <div class="img-container">
      <img src="../assets/images/home-5-image-box-01.png" alt="" />
    </div>
    <div class="card-title">
      <h4>Idea Discussion</h4>
    </div>
    <div class="card-text">
      <span
        >Lorem ipsum dolor sit amet consectetur adipisicing elit. Similique
        reiciendis corporis ipsum excepturi earum.</span
      >
    </div>
    <div class="card-link">
      <a
        >Start now <span><i class="fas fa-long-arrow-alt-right"></i></span
      ></a>
    </div>
  </li>
</template>

<script>
export default {
  name: "StartingCard",
};
</script>

<style lang="scss" scoped>
li {
  padding: 50px;
  .card-title {
    margin-bottom: 0.5rem;
  }

  .card-text {
    color: #959999;
    line-height: 1.5rem;
    margin-bottom: 1rem;
  }

  .card-link {
    color: #96a6a5;
    font-weight: bold;
  }
}
</style>
