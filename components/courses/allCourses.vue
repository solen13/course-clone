<template>
<div class="Courses-companet">

 <content-head title="Course content" sub-title="Live" buttonview="Choose day" btn-bg="#B4975A" text-color="#FFFFFF"/>

  <ul>
    <li>
      <nuxt-link class="nuxtlink" to="/courses/selection" v-for="item in 5" :key="item">
        <img src="../../static/icon/right.svg">
        <span>What’s Islam?</span>
      </nuxt-link>
    </li>
  </ul>

</div>
</template>

<script>
import ContentHead from "../contentHead/content-head";
export default {
  name: "allCourses",
  components: {ContentHead},
}
</script>

<style lang="scss" scoped>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.Courses-companet{
  width: 880px;
  height: 500px;
  border: 1px solid #EBEEF3;
  border-radius: 8px;
  padding: 40px;
  ul{
    li{
      display: flex;
      flex-flow: column;
      list-style: none;
      border: 1px solid #EBEEF3;
      border-radius: 8px;
      .nuxtlink{
        width: 100%;
        padding: 24px;
        border-bottom: 1px solid #EBEEF3;
        text-decoration: none;
        span{
          color: #425466;
          margin-left: 20px;
        }
      }
      .nuxtlink:last-child{
        border: none;
      }

    }
  }
}
</style>
