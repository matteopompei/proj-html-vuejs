<template>
  <main>
    <FirstLesson />
    <Telephone />
    <Courses />
    <Rates />
    <Instructors />
  </main>
</template>

<script>
import FirstLesson from "../sections/FirstLesson.vue";
import Telephone from "../sections/Telephone.vue";
import Courses from "../sections/Courses.vue";
import Rates from "../sections/Rates.vue";
import Instructors from "../sections/Instructors.vue";

export default {
  name: "Main",
  components: {
    FirstLesson,
    Telephone,
    Courses,
    Rates,
    Instructors,
  },
};
</script>

<style lang="scss" scoped></style>
