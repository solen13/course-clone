<template>
  <div class="myCertificates">
    <h3>My Certificates</h3>
    <ul>
      <li v-for="item in 3 " :key="item">
        <img src="../../static/certificates.png" alt="">
        <div class="myCertificates-overlay">
        <span> Level 1</span>
        </div>
      </li>
    </ul>

  </div>
</template>

<script>
export default {
  name: "myCertificates",

}
</script>

<style lang="scss" scoped>
.myCertificates{
  width: 100%;

  height: 400px;
  padding: 40px;
  h3{
    font-size:24px;
    color: #425466;
    margin-bottom: 24px;
  }
  ul{
    display: flex;
    flex-flow: wrap;
    gap: 10px;
    li{
      list-style: none;
      display: flex;
       flex-flow: column;

      img{
         width: 250px;
        height: 200px;
        border-radius: 8px;
        position: relative;
      }
      .myCertificates-overlay{
        width: 250px;
        height: 68px;
       background:linear-gradient(to top ,rgba(0, 0, 0, 0.95),#00000000);
        position: absolute;
       margin-top:132px ;
        display: flex;
        align-items: center;
        justify-content: flex-start;
       span{
         color: #FFFFFF;
         font-size: 18px;
         font-weight: bold;
        margin-left: 24px;
       }
      }
    }
  }
}
</style>
