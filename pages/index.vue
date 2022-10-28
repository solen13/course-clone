<template>

  <div class="content" >


    <Banner/>
    <Livecorse/>
    <OutCourse/>
    <comment/>
    <new-articles/>
   <accordion-main-case/>

    <ib-modal>
      <login/>
      </ib-modal>


  </div>

</template>

<script>


import OutCourse from "../components/homePage/ourCourse";
import Comment from "../components/homePage/comment";
import Footer from "../components/header-footer/Footer";
import NewArticles from "../components/homePage/newArticles";
import Login from "../components/login/login";
import IbModal from "../components/modal/ib-modal";
import Accordion from "../components/accordion/accordion";
import Livecorse from "../components/homePage/Live-corse";
import Banner from "../components/homePage/Banner";
import AccordionMainCase from "../components/accordion/accordion-main-page";
export default {
  name: 'IndexPage',
  components: {AccordionMainCase, Accordion, IbModal, Login, NewArticles, Footer, Comment, OutCourse,Livecorse,Banner},
  data(){
    return{
      data:'flex'
    }
  },
  props:{

  },
  methods:{

  },
computed:{

}

}
</script>
<style scoped lang="scss">
.content{
  position: relative;
  .login-copmanet{
    position: fixed;
    top: 0;
  }
}
</style>
