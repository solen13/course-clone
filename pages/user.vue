<template>
<div class="users">
  <div class="banner">
    <left-comment/>
    <nuxt-child class="nuxt-child"/>
  </div>

</div>
</template>

<script>
import LeftComment from "../components/profile/leftComment";
export default {
  name: "user",
  components: {LeftComment},
}
</script>

<style lang="scss" scoped>
.users{
  width: 100%;
  height: 600px;
  display: flex;
  align-items: center;
  justify-content: center;
  .banner{
    display: flex;
    height: 80%;

    .nuxt-child{
      width: 880px;
      margin-left: 20px;
      border-radius: 8px;
      border: 1px solid #EBEEF3;
      background-color: #FFFFFF;
      padding: 40px;
    }
  }

}
</style>
