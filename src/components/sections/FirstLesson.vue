<template>
  <section>
    <div class="container">
      <div class="left">
        <div class="title">Get Behind The Wheel</div>
        <div class="subtitle">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc ultrices
          auctor sapien id cursus. Aliquam maximus turpis in vehicula semper.
        </div>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc ultrices
          auctor sapien id cursus. Aliquam maximus turpis in vehicula semper.
          Fusce et ultrices libero, at suscipit lacus. Sed vitae fringilla nibh.
          Nunc ultrices auctor sapien id cursus. Aliquam maximus turpis in
          vehicula semper. Fusce et ultrices libero, at suscipit lacus. Sed
          vitae fringilla nibh.
        </p>
      </div>
      <div class="right">
        <div class="form">
          <div class="title">First Lesson Free!</div>
          <p>
            When you make a block booking with us your first lesson is included
            free.
          </p>
          <form>
            <input type="text" placeholder="Your Name*" />
            <input type="email" placeholder="Email*" />
            <input type="text" placeholder="Telephone" />
            <input type="text" placeholder="Location" />
            <input type="submit" value="Request a callback" class="button" />
          </form>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "FirstLesson",
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

section {
  margin-bottom: -50px;
  padding: 100px 0 0 0;

  .left,
  .right {
    width: 50%;
  }

  .left {
    .title {
      margin-bottom: 50px;
      font-size: 2.5rem;
      font-weight: bold;
      color: $color1;
    }
    .subtitle {
      margin-bottom: 50px;
      font-size: 1.5rem;
      color: $color2;
      line-height: 2.5rem;
    }

    p {
      color: $color2;
      line-height: 2rem;
    }
  }

  .right {
    transform: translateY(-150px);

    .form {
      margin: 0 auto;
      padding: 70px 30px;
      width: 90%;
      background: #fff;
      border-radius: 20px;
      box-shadow: $box-shadow;
      text-align: center;

      .title {
        margin-bottom: $box-border-radius;
        font-size: 2rem;
        font-weight: bold;
        color: $accent;
      }

      p {
        margin-bottom: 30px;
        font-size: 1rem;
        color: $color2;
        line-height: 2rem;
      }

      input[type="text"],
      input[type="email"] {
        margin-bottom: 30px;
        padding: 15px 15px;
        width: 100%;
        background: #f6f6f6;
        border: 1px solid #d9d9d9;
        border-radius: 5px;
        outline: none;
        font-family: $first-font;
        font-size: 0.8rem;
        color: $color2;
      }

      .button {
        cursor: pointer;
      }
    }
  }
}
</style>
