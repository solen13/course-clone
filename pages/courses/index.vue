<template>
<div class="corses">

  <all-courses/>
</div>
</template>

<script>
import AllCourses from "../../components/courses/allCourses";
export default {
  name: "index",
  components: {AllCourses}
}
</script>

<style scoped>
.corses{
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 20px;
  margin-bottom: 20px;
}
</style>
