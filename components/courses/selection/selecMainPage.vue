<template>
<div>
  <template v-for="item in list">
    <course-selection :item="item" :key="item"/>
  </template>

</div>
</template>

<script>
import lists from "../../../constants/chooseDay"
import CourseSelection from "./courseSelection";
export default {
  name: "selecMainPage",
  components: {CourseSelection},
  data(){
    return{
      list:null
    }
  },
  mounted() {
    this.list=lists
  }
}
</script>

<style scoped>

</style>
