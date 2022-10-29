<template>

  <div class="container">
    <content-head title="Course content" sub-title="Live" buttonview="You’re already joined"  />

    <ul>
      <li v-for="item in 5" :key="item">

        <span>
          <img src="../../../static/icon/play.png" alt="">
          <p>What’s Islam?</p>
        </span>
        <p>07:24</p>
      </li>
    </ul>

  </div>
</template>

<script>
import ContentHead from "../../contentHead/content-head";
export default {
  name: "coursesDetail",
  components: {ContentHead}
}
</script>

<style lang="scss" scoped>
.container{
  width: 880px;
  height: 514px;
  padding: 40px;
  border: 1px solid #EBEEF3;
  margin-bottom: 20px;
  margin-top: 20px;
  ul{
    border: 1px solid #EBEEF3;

    li{
      display: flex;
      justify-content: space-between;
      padding: 24px;
      border-bottom: 1px solid #EBEEF3;
      cursor: pointer;
      span{
        display: flex;
        align-items: center;
        p{
          color: #425466;
          margin-left: 10px;
        }
      }
    }
    li:last-child{
      border: none;
    }
  }
}
</style>
