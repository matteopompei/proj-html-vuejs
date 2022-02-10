<template>
  <section>
    <div class="container">
      <div class="credits">
        © Copyright 2012 - 2022 | Avada Theme by <a href="#">ThemeFusion</a> |
        All Rights Reserved | Powered by <a href="#">WordPress</a>
      </div>
      <div class="social">
        <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
        <a href="#"><i class="fa-brands fa-twitter"></i></a>
        <a href="#"><i class="fa-brands fa-youtube"></i></a>
        <a href="#"><i class="fa-brands fa-instagram"></i></a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Credits",
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

section {
  padding: 70px 0;
  background: #333333;

  .credits {
    font-size: 0.8rem;
    color: $color2;

    a {
      text-decoration: none;
      color: $accent;
    }
  }

  .social {
    font-size: 1.2rem;

    a {
      margin: 0 10px;
      color: #fff;
      transition: $trans-time;

      &:hover {
        color: rgba(119, 153, 173, 0.8);
      }
    }
  }
}
</style>
