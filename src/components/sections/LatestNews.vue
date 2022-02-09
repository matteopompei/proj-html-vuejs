<template>
  <section>
    <div class="container">
      <div>
        <div class="title">Latest News</div>
        <div class="news">
          <div
            class="article"
            v-for="(element, index) in articles"
            :key="index"
          >
            <div class="img">
              <a href="#"><img :src="element.img" :alt="element.title" /></a>
            </div>
            <a href="#" class="title">{{ element.title }}</a>
            <div class="info">
              {{ element.date }} |
              <a href="#">{{ element.comments }} Comments</a>
            </div>
            <p>{{ element.text }}</p>
          </div>
        </div>
        <a href="#" class="more">More from the blog</a>
      </div>

      <svg
        class="fusion-big-triangle-candy"
        xmlns="http://www.w3.org/2000/svg"
        version="1.1"
        width="100%"
        height="100"
        viewBox="0 0 100 100"
        preserveAspectRatio="none"
        style="fill: #fff; padding: 0"
      >
        <path d="M-1 -1 L50 99 L101 -1 Z"></path>
      </svg>
    </div>
  </section>
</template>

<script>
import articlesArr from "../../assets/data/articles.js";

export default {
  name: "LatestNews",
  data() {
    return {
      articles: articlesArr,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

section {
  padding: 100px 0;
  background: url("../../assets/img/latestnews-background.jpg") center;
  background-size: cover;

  .container {
    flex-direction: column;

    & > div {
      margin-top: -80px;
      padding: 70px 50px;
      background: #fff;
      border-top: 5px solid #929aa3;
      border-radius: 10px 10px 0 0;
      box-shadow: -25px 20px 30px rgba(0, 0, 0, 0.2),
        25px 20px 30px rgba(0, 0, 0, 0.2);
      transform: translateY(-50px);
      text-align: center;

      .title {
        font-size: 2.5rem;
        font-weight: bold;
        color: $color1;
      }

      .news {
        display: flex;
        justify-content: space-between;
        gap: 30px;
        margin: 50px auto;

        .article {
          .img {
            overflow: hidden;
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
            display: block;
            margin: 10px 0;
            font-size: 1.3rem;
          }

          .info {
            margin-bottom: 30px;
            font-size: 0.7rem;
            color: $color2;
          }

          a {
            text-decoration: none;
            color: $accent;
          }

          p {
            color: $color2;
          }
        }
      }

      .more {
        display: block;
        margin: 30px auto;
        padding: 13px 30px;
        height: fit-content;
        width: fit-content;
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

    svg {
      z-index: 1;
      position: relative;
      width: 100%;
      margin-top: -50px;
    }
  }
}
</style>
