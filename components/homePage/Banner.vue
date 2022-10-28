<template>
<div class="contener-bacgrand">

  <div class="content">
    <h1>Islam for Beginners</h1>

    <p>Is a free online education service run by The Foundation of Light,
      Spirituality and Arts - a local charity based in the UK
      . We aim to deliver free, online and quality education
      for all those who are interested in Islam.
    </p>

   <ib-button :outlined="true" text="Discover" bg-color="#B4975A"  text-color="#FFFFFF" :round="true"/>

  </div>



</div>
</template>

<script>

export default {
  name: "Banner",

}
</script>

<style  lang="scss" scoped >
$primary: rgba(45, 43, 116, 0.62);
.contener-bacgrand{


width: 100%;
  height: 450px;
background-image:url("../../static/bannerBacgrand.png") ;

  .content{
    width: 100%;
    height: 100%;
   background-color: $primary;
    color:#FFFFFF ;
    display: flex;
    flex-flow: column;
    align-items: center;
    justify-content: center;
    h1{
      margin-bottom: 24px;
      font-size: 48px;
      font-weight: 700;
      line-height: 57px;
    }
    p{
      width: 580px;
      margin-bottom: 24px;

      font-weight: 400;
      font-size: 16px;
      line-height: 24px;
      text-align: center;
    }

  }


}

</style>
