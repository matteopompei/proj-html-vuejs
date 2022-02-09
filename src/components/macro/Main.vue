<template>
  <main>
    <FirstLesson />
    <Telephone />
    <Courses />
    <Rates />
    <Instructors />
    <Testimonials />
    <LatestNews />
  </main>
</template>

<script>
import FirstLesson from "../sections/FirstLesson.vue";
import Telephone from "../sections/Telephone.vue";
import Courses from "../sections/Courses.vue";
import Rates from "../sections/Rates.vue";
import Instructors from "../sections/Instructors.vue";
import Testimonials from "../sections/Testimonials.vue";
import LatestNews from "../sections/LatestNews.vue";

export default {
  name: "Main",
  components: {
    FirstLesson,
    Telephone,
    Courses,
    Rates,
    Instructors,
    Testimonials,
    LatestNews,
  },
};
</script>

<style lang="scss" scoped></style>
