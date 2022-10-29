<template>
<div class="contener">
<course-selection/>
</div>
</template>

<script>

import CourseSelection from "../../../components/courses/selection/courseSelection";
import SelecMainPage from "../../../components/courses/selection/selecMainPage";
export default {
  name: "index",
  components: {SelecMainPage, CourseSelection}
}
</script>

<style scoped>
.contener{
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
