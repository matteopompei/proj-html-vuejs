<template>
  <section>
    <div class="container">
      <div class="title">Testimonials</div>
      <div class="subtitle">
        Here’s what our happy drivers had to say about our services:
      </div>
      <div v-for="(element, index) in testimonials" :key="index">
        <div class="testimonials" v-show="index == current">
          <img :src="element.img" alt="element.name" />
          <blockquote>
            {{ element.quote }}
          </blockquote>
          <div class="name">{{ element.name }}</div>
        </div>
      </div>
      <div>
        <div
          class="slide"
          :class="{ active: index == current }"
          @click="current = index"
          v-for="(element, index) in testimonials"
          :key="index"
        ></div>
      </div>
    </div>
  </section>
</template>

<script>
import testimonialsArr from "../../assets/data/testimonials.js";

export default {
  name: "Testimonials",
  data() {
    return {
      testimonials: testimonialsArr,
      current: 0,
      time: null,
    };
  },
  mounted: function () {
    this.startSlide();
  },
  methods: {
    startSlide() {
      this.timer = setInterval(this.next, 5000);
    },
    next() {
      this.current += 1;
      if (this.current == this.testimonials.length) {
        this.current = 0;
      }
    },
    prev() {
      this.current -= 1;
      if (this.current > 0) {
        this.current = this.testimonials.length;
      }
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

section {
  background: url("../../assets/img/testimonial-background.jpg") center;
  background-size: cover;

  .container {
    flex-direction: column;
    text-align: center;
    padding: 200px 0;

    .title {
      margin-bottom: 10px;
      font-size: 2.5rem;
      font-weight: bold;
      color: $color1;
    }

    .subtitle {
      font-size: 1.4rem;
      color: $color2;
    }

    .testimonials {
      margin: 50px auto;
      animation: fade $trans-time forwards;

      img {
        margin: auto;
        width: 150px;
      }

      blockquote {
        margin: 30px auto;
        width: 50%;
        font-size: 1.1rem;
        font-style: italic;
        letter-spacing: 3px;
        line-height: 2rem;
        color: $color2;
      }

      .name {
        font-size: 1.1rem;
        font-weight: bold;
        letter-spacing: 3px;
        color: $color2;
      }

      @keyframes fade {
        from {
          opacity: 0;
        }
        to {
          opacity: 1;
        }
      }
    }

    .slide {
      display: inline-block;
      margin: 0 5px;
      height: 12px;
      width: 12px;
      background: transparent;
      border: 1px solid $color2;
      border-radius: 50%;
      cursor: pointer;
      transition: $trans-time;

      &.active {
        background: $color2;
      }
    }
  }
}
</style>
