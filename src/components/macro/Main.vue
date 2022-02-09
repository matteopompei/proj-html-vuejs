<template>
  <main>
    <FirstLesson />
    <Telephone />
    <Courses />
    <Rates />
    <Instructors />
    <Testimonials />
  </main>
</template>

<script>
import FirstLesson from "../sections/FirstLesson.vue";
import Telephone from "../sections/Telephone.vue";
import Courses from "../sections/Courses.vue";
import Rates from "../sections/Rates.vue";
import Instructors from "../sections/Instructors.vue";
import Testimonials from "../sections/Testimonials.vue";

export default {
  name: "Main",
  components: {
    FirstLesson,
    Telephone,
    Courses,
    Rates,
    Instructors,
    Testimonials,
  },
};
</script>

<style lang="scss" scoped></style>
