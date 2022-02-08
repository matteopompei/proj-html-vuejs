<template>
  <header>
    <div class="top-bar">
      <div class="container">
        <span>We have a 95% Successful Pass Rate!</span>
        <span
          ><i class="fa-solid fa-phone"></i> Give us a call to book your
          tuition! 1-800-555-555</span
        >
      </div>
    </div>
    <section class="jumbo">
      <Navbar :menu="menu" />
      <div class="container">
        <div class="title">Drive with Avada</div>
        <div class="subtitle">
          We offer the finest driving tuition money can buy
        </div>
      </div>
    </section>
  </header>
</template>

<script>
import Navbar from "../sections/Navbar.vue";
import menuArr from "../../assets/data/menu.js";

export default {
  name: "Header",
  components: {
    Navbar,
  },
  data() {
    return {
      menu: menuArr,
    };
  },
};
</script>

<style lang="scss" scoped>
.top-bar {
  padding: 15px 0;
  background: #333333;

  span {
    font-size: 0.8rem;
    color: #7799ad;

    .fa-phone {
      transform: translateX(-10px);
    }
  }
}

.jumbo {
  position: relative;
  padding: 20% 0 10% 0;
  background: url("../../assets/img/homepage-hero-background.jpg");
  background-size: cover;
  color: #fff;

  .container {
    justify-content: flex-start;
    flex-direction: column;
  }
  .title {
    font-size: 3.6rem;
    font-weight: bold;
  }

  .subtitle {
    font-size: 1.4rem;
  }
}
</style>
