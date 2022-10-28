<template>
  <div class="questions-contener">
    <slider-questions/>

    <span>
      <nuxt-child class="nuxtChlid"/>
      <Share/>
    </span>

  </div>
</template>

<script>
import SliderQuestions from "../components/questions/sliderQuestions";
import Share from "../components/questions/share";
export default {
  name: "questions",
  components: {Share, SliderQuestions}
}
</script>

<style lang="scss" scoped>
 .questions-contener{
   display: flex;
   margin-top: 20px;
   margin-bottom: 20px;
   border-radius: 8px;
   span{
     border-radius: 8px;
     width: 880px;
     padding: 40px;
     border: 1px solid #EBEEF3;
     margin-left: 20px;
     .nuxtChlid{
      width: 100%;

     }
   }

 }
</style>
