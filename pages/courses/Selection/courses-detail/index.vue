<template>
<div class="detail">
  <courses-detail/>
</div>
</template>

<script>
import CoursesDetail from "../../../../components/courses/detail/coursesDetail";
export default {
  name: "index",
  components: {CoursesDetail}
}
</script>

<style scoped>
.detail{
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
