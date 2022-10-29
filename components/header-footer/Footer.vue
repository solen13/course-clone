<template>
  <div class="footer">

    <div class="logo">  <img src="../../static/Foundation.png">  </div>


    <div class="icons">
      <ib-button @clicked="$router.push('/')" class="ib-button" margin="5px" icon="home"  direction="left"  text="HOME" text-color="#EBEEF3"  />
      <ib-button @clicked="$router.push('/courses')"  margin="5px"  icon="icon3"  direction="left"  text="COURSES" text-color="#EBEEF3"  />
      <ib-button  @clicked="$router.push('/questions/privacy-policy')"  margin="5px"  icon="icon4"  direction="left"  text="QUESTIONS" text-color="#EBEEF3"  />


    </div>

    <div class="sosical">
      <ul>
        <li><ib-button icon="sosyalIcon2" direction="left" " /></li>
        <li> <ib-button icon="sosyalIcon1" direction="left" /></li>
        <li> <ib-button icon="sosyalIcon3" direction="left" /></li>
        <li> <ib-button icon="sosyalIcınyoutube" direction="left" /></li>

      </ul>

    </div>

  </div>
</template>

<script>
import ibButton from "../button/ib-button";
export default {
  name: "Footer",
  components:{
    ibButton
  }
}
</script>

<style lang="scss" >


*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.footer{
  width: 100%;
  height:176px ;
  background-color: #2D2B74;
  display: flex;
  justify-content: space-around;
  align-items: center;
  background-image:url("../../static/footerBg.png");
  background-repeat: no-repeat;
  .logo{
    img{
      width: 180px;
      height:112px ;
  }

  }

  .icons{
    display: flex;
    .ib-button{
      margin-left:50px ;
    }
    .ib-button:first-child{
      margin-left:0 ;
    }
  }

  .sosical{
    ul{
      display: flex;
      li{
        width:48px;
        height: 48px;
        background-color: #FFFFFF;
        border-radius: 100%;
        list-style: none;
        margin-left: 16px;
        display: flex;
        align-items: center;
        justify-content: center;
      }
    }
  }

}



</style>
