<template>
  <section>
    <div class="container">
      <div>
        <img
          src="../../assets/img/avada-drivers-logo-1x.png"
          alt="Avada Driving School"
          class="logo"
        />
        <p>
          Avada Driving School is the right choice for experienced drivers
          looking for a refresher course, or the brand new driver wanting to
          pass first time.
        </p>
      </div>
      <div class="contacts">
        <div class="title">Contact details</div>
        <ul>
          <li>
            <i class="fa-solid fa-house-chimney"></i> 12345 North Main Street,
            New York, NY 555555
          </li>
          <li><i class="fa-solid fa-phone"></i> 1.800.555.6789</li>
          <li><i class="fa-regular fa-envelope"></i> info@your-domain.com</li>
          <li><i class="fa-solid fa-link"></i> Theme-Fusion.com</li>
        </ul>
      </div>
      <div class="courses">
        <div class="title">Courses</div>
        <ul>
          <li v-for="(element, index) in courses" :key="index">
            <i class="fa-regular fa-circle-right"></i
            ><a :href="element.src">{{ element.text }}</a>
          </li>
        </ul>
      </div>
      <div style="text-align: center">
        <img
          src="../../assets/img/footer-ad-grid-400x357.webp"
          alt=""
          class="ad-grid"
        />
        <a href="#" class="button">Book now</a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Recap",
  props: {
    courses: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

section {
  padding: 70px 0;
  background: url("../../assets/img/footer-background-color.jpg") center;
  background-size: center;

  .container {
    & > div {
      width: 20%;
      font-size: 0.85rem;
      line-height: 1.5rem;
      color: $color2;

      .title {
        margin-bottom: 30px;
        font-size: 1rem;
        font-weight: bold;
        text-transform: uppercase;
        color: #fff;
      }

      img {
        width: 100%;
      }

      .logo {
        margin-bottom: 10px;
      }

      .ad-grid {
        margin-bottom: 25px;
      }
    }
    .contacts {
      ul {
        list-style: none;

        li {
          margin: 15px 0;
          padding-left: 30px;

          svg {
            display: inline-block;
            color: #bbcbd3;
            margin-left: -21px;
            height: 16px;
            transform: translateX(-10px);
          }
        }
      }
    }
    .courses {
      ul {
        list-style: none;

        li {
          margin: 15px 0;
          padding-left: 30px;

          a {
            font-size: 1.1rem;
            text-decoration: none;
            color: $accent;
          }

          svg {
            display: inline-block;
            color: $accent;
            margin-left: -21px;
            height: 16px;
            transform: translateX(-10px);
          }
        }
      }
    }
  }

  // .logo {
  //   width: 220px;
  // }
}
</style>
