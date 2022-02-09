<template>
  <section>
    <div class="container">
      <div class="card">
        <div class="number">95%</div>
        <div class="title">Pass rate</div>
      </div>
      <div class="card">
        <div class="number">100%</div>
        <div class="title">Referral rate</div>
      </div>
      <div class="card">
        <div class="number">0%</div>
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
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 100px;
    margin: 10px;
    min-height: 350px;
    width: 30%;
    background: #fff;
    border-top: 5px solid $accent;
    border-radius: $box-border-radius;
    box-shadow: $box-shadow;
    transform: translateY(-50px);
    text-align: center;

    .number {
      font-size: 3rem;
      color: $color2;
    }

    .title {
      font-size: 0.9rem;
      font-weight: bold;
      text-transform: uppercase;
      color: $color2;
    }
  }
}
</style>
