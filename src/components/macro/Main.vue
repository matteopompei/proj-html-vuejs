<template>
  <main>
    <FirstLesson />
    <Telephone />
    <Courses />
    <Rates />
    <Instructors />
    <Testimonials />
    <LatestNews />
    <Newsletter />
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
import Newsletter from "../sections/Newsletter.vue";

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
    Newsletter,
  },
};
</script>

<style lang="scss" scoped></style>
