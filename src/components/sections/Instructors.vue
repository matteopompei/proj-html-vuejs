<template>
  <section>
    <div class="container">
      <div>
        <div class="title">Your Instructors</div>
        <div class="subtitle">
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc
            ultrices auctor sapien id cursus. Aliquam maximus turpis in vehicula
            semper.
          </p>
          <a href="#" class="about-us">More about us</a>
        </div>
      </div>
      <div class="instructors">
        <div class="card" v-for="(element, index) in instructors" :key="index">
          <img :src="element.img" alt="element.name" />
          <div class="name">{{ element.name }}</div>
          <div class="social">
            <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
            <a href="#"><i class="fa-brands fa-twitter"></i></a>
            <a href="#"><i class="fa-brands fa-instagram"></i></a>
          </div>
          <p>{{ element.text }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import instructorsArr from "../../assets/data/instructors.js";

export default {
  name: "Instructors",
  data() {
    return {
      instructors: instructorsArr,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

section {
  padding-top: 50px;

  .container {
    flex-direction: column;

    .title {
      margin-bottom: 50px;
      font-size: 2.5rem;
      font-weight: bold;
      color: $color1;
    }

    .subtitle {
      display: flex;
      justify-content: space-between;
      gap: 50px;
      margin-bottom: 100px;

      p {
        width: 60%;
        font-size: 1.3rem;
        line-height: 2.5rem;
        color: $color2;
      }

      .about-us {
        // display: block;
        padding: 13px 100px;
        height: fit-content;
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

    .instructors {
      display: flex;
      gap: 15px;

      .card {
        display: flex;
        flex-direction: column;
        justify-content: center;
        gap: 15px;
        padding: 35px 30px;
        width: 33%;
        background: #fff;
        border-top: 5px solid $accent;
        border-radius: $box-border-radius;
        box-shadow: $box-shadow;
        transform: translateY(-50px);
        text-align: center;

        img {
          transition: 0.3s;

          box-shadow: 0 0 15px rgba(0, 0, 0, 0);
          &:hover {
            transform: scale(1.02);
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.5);
          }
        }

        .name {
          font-size: 1.5rem;
          font-weight: bold;
          color: $color1;
        }

        .social {
          a {
            margin: 0 10px;
            color: $color2;
          }
        }

        p {
          margin-bottom: 30px;
          line-height: 2rem;
          color: $color2;
        }
      }
    }
  }
}
</style>
