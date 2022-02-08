<template>
  <section>
    <div class="container">
      <div class="left">
        <div class="info">
          <div class="title">Courses</div>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc
            ultrices auctor sapien id cursus. Aliquam maximus turpis in vehicula
            semper.
          </p>
          <a href="#">Course information</a>
        </div>
      </div>
      <div class="right">
        <div class="courses">
          <div v-for="(element, index) in courses" :key="index">
            <div class="img">
              <img :src="element.img" alt="element.text" />
            </div>
            <div class="title">{{ element.text }}</div>
            <a href="#">Learn more</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import coursesArr from "../../assets/data/courses.js";

export default {
  name: "Courses",
  data() {
    return {
      courses: coursesArr,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

section {
  background: url("../../assets/img/promise-background.jpg") bottom;
  background-size: cover;

  .left {
    width: 40%;

    .info {
      padding: 70px 50px;
      background: #fff url("../../assets/img/new-corner.jpg") no-repeat top left;
      background-size: 100px;
      border-radius: 20px;
      box-shadow: $box-shadow;
      text-align: center;
      transform: translateY(-30px);

      .title {
        margin-bottom: 50px;
        font-size: 2.5rem;
        font-weight: bold;
        color: $color1;
      }

      p {
        margin-bottom: 50px;
        font-size: 1rem;
        line-height: 2rem;
        color: $color2;
      }

      a {
        padding: 13px 30px;
        background: $accent;
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

  .right {
    width: 60%;
    margin-left: 50px;

    .courses {
      padding: 70px 0;
      display: flex;
      justify-content: space-between;

      & > div {
        text-align: center;

        .img {
          margin-bottom: 20px;
          height: 200px;
          width: 200px;
          overflow: hidden;
          background: #fff;

          img {
            height: 100%;
            width: 100%;
            transition: 1s;

            &:hover {
              transform: scale(1.1);
              opacity: 0.9;
            }
          }
        }

        .title {
          margin-bottom: 25px;
          font-size: 1.4rem;
          font-weight: bold;
          color: $color2;
        }

        a {
          padding: 10px 20px;
          border: 3px solid $color2;
          border-radius: $button-border-radius;
          font-size: 0.7rem;
          font-weight: bold;
          color: $color2;
          text-transform: uppercase;
          text-decoration: none;
          transition: $trans-time;

          &:hover {
            color: $accent;
            border-color: $accent;
          }
        }
      }
    }
  }
}
</style>
