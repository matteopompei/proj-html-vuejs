<template>
  <main>
    <FirstLesson />
    <Telephone />
  </main>
</template>

<script>
import FirstLesson from "../sections/FirstLesson.vue";
import Telephone from "../sections/Telephone.vue";

export default {
  name: "Main",
  components: {
    FirstLesson,
    Telephone,
  },
};
</script>

<style lang="scss" scoped></style>
