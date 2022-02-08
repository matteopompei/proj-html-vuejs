<template>
  <main>
    <FirstLesson />
    <Telephone />
    <Courses />
  </main>
</template>

<script>
import FirstLesson from "../sections/FirstLesson.vue";
import Telephone from "../sections/Telephone.vue";
import Courses from "../sections/Courses.vue";

export default {
  name: "Main",
  components: {
    FirstLesson,
    Telephone,
    Courses,
  },
};
</script>

<style lang="scss" scoped></style>
