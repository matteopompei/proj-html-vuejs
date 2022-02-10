<template>
  <section>
    <div class="container">
      <div class="card">
        <div class="circle">
          <svg>
            <circle cx="110" cy="110" r="100"></circle>
            <circle cx="110" cy="110" r="100"></circle>
          </svg>
          <div class="number">95%</div>
        </div>
        <div class="title">Pass rate</div>
      </div>
      <div class="card">
        <div class="circle">
          <svg>
            <circle cx="110" cy="110" r="100"></circle>
            <circle cx="110" cy="110" r="100"></circle>
          </svg>
          <div class="number">100%</div>
        </div>
        <div class="title">Referral rate</div>
      </div>
      <div class="card">
        <div class="circle">
          <svg>
            <circle cx="110" cy="110" r="100"></circle>
            <circle cx="110" cy="110" r="100"></circle>
          </svg>
          <div class="number">0%</div>
        </div>
        <div class="title">Accident rate</div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Rates",
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

section {
  background: url("../../assets/img/driving-triangle.svg") no-repeat center top;
  background-size: 100% 100px;

  .card {
    margin: 10px;
    padding: 50px 0;
    width: 33%;
    background: #fff;
    border-top: 5px solid $accent;
    border-radius: $box-border-radius;
    box-shadow: $box-shadow;
    transform: translateY(-50px);
    text-align: center;

    .circle {
      position: relative;
      .number {
        position: absolute;
        top: 40%;
        left: 50%;
        transform: translate(-50%, -50%);
        font-size: 3rem;
        color: $color2;
      }

      svg {
        margin-bottom: 50px;
        height: 220px;
        width: 220px;
        transform: rotate(-90deg);

        & > circle {
          height: 100%;
          width: 100%;
          fill: none;
          stroke-width: 10;
          stroke-linecap: round;
          stroke: #f6f6f6;

          &:nth-child(2) {
            stroke: $accent;
            stroke-dasharray: 630px;
            stroke-dashoffset: 630px;
          }
        }
      }
    }

    .title {
      font-size: 1rem;
      font-weight: bold;
      text-transform: uppercase;
      color: $color2;
    }

    &:nth-child(1) {
      .circle {
        svg {
          & > circle {
            &:nth-child(2) {
              stroke-dashoffset: calc(630px - (630px * 95) / 100);
            }
          }
        }
      }
    }
    &:nth-child(2) {
      .circle {
        svg {
          & > circle {
            &:nth-child(2) {
              stroke-dashoffset: calc(630px - (630px * 100) / 100);
            }
          }
        }
      }
    }
    &:nth-child(3) {
      .circle {
        svg {
          & > circle {
            &:nth-child(2) {
              stroke-dashoffset: calc(630px - (630px * 0.01) / 100);
            }
          }
        }
      }
    }
  }
}
</style>
