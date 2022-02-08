<template>
  <section>
    <div class="container">
      <div class="left">
        <div class="title">Start Learning to Drive Today</div>
        <div class="subtitle">
          Give us a call to schedule your first driving lesson
        </div>
      </div>
      <div class="right">
        <div class="phone"><i class="fa-solid fa-phone"></i> 1-800-555-555</div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Telephone",
};
</script>

<style lang="scss" scoped>
section {
  padding: 100px 0;
  background: url("../../assets/img/horizontal-cta-background.jpg") center;
  background-size: cover;
  color: #fff;

  .container {
    align-items: center;

    .title {
      margin-bottom: 20px;
      font-size: 2.7rem;
      font-weight: bold;
    }

    .subtitle {
      font-size: 1.4rem;
      font-weight: bold;
    }

    .phone {
      font-size: 2rem;

      .fa-phone {
        transform: translateX(-20px);
      }
    }
  }
}
</style>
