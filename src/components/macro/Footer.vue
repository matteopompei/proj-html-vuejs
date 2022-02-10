<template>
  <footer>
    <Recap :courses="courses" />
    <Credits />
  </footer>
</template>

<script>
import coursesArr from "../../assets/data/courses-footer.js";
import Recap from "../sections/Recap.vue";
import Credits from "../sections/Credits.vue";

export default {
  name: "Footer",
  components: {
    Recap,
    Credits,
  },
  data() {
    return {
      courses: coursesArr,
    };
  },
};
</script>

<style lang="scss" scoped></style>
