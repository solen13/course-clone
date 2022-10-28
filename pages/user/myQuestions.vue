<template>
<div class="questions">
  <h3>My Questions</h3>
  <ul>
    <li v-for="item in 6" :key="item">
      <p>Kainat Hz. Muhammed’in (asm) hürmetine mi yaratıldı? </p>
      <label>aNswered 2 days ago</label>
    </li>
  </ul>

</div>
</template>

<script>
export default {
  name: "questions",

}
</script>

<style lang="scss" scoped>
.questions{
  width: 100%;
  height: 400px;
  padding: 40px;
  h3{
    font-size: 24px;
    color: #425466;
    margin-bottom: 24px;

  }
  ul{
    display: flex;
    flex-flow: wrap;
   gap: 10px;
    li{
      width: 250px;
      height: 120px;
      border: 1px solid #EBEEF3;
      border-radius: 8px;
      padding-right: 24px;
      padding-left: 24px;
     padding-top: 16px;
  list-style: none;


      p{
        color: #425466;
        font-size: 16px;
        margin-bottom: 8px;
        font-weight:600;
      }
      label{
      color: #6C7C8C;
        font-size: 10px;
      }

    }
  }
}
</style>
