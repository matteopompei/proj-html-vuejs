<template>
  <section>
    <div class="container">
      <div class="title">Sign up to our Newsletter</div>
      <input type="text" />
      <input type="submit" value="Subscribe" />
      <p>
        (We do not share your data with anybody, and only use it for its
        intended purpose)
      </p>
    </div>
  </section>
</template>

<script>
export default {
  name: "Newsletter",
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

section {
  background: url("../../assets/img/newsletter_background.jpg") center;
  background-size: cover;

  .container {
    flex-direction: column;
    align-items: center;
    padding: 50px 0;

    .title {
      margin-bottom: 25px;
      font-size: 2rem;
      font-weight: bold;
      color: $color1;
    }

    input[type="text"] {
      margin-bottom: 30px;
      padding: 15px 15px;
      width: 600px;
      background: #f6f6f6;
      border: 1px solid #d9d9d9;
      border-radius: 3px;
      outline: none;
      font-family: $first-font;
      font-size: 0.8rem;
      color: $color2;
    }

    input[type="submit"] {
      display: block;
      margin-bottom: 50px;
      padding: 13px 30px;
      height: fit-content;
      width: 600px;
      background: $accent;
      border: none;
      border-radius: $button-border-radius;
      font-size: 1.4;
      font-weight: bold;
      text-decoration: none;
      text-transform: uppercase;
      color: #fff;
      transition: $trans-time;

      &:hover {
        background: $accent-hover;
      }
    }
  }
}
</style>
