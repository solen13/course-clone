<template>
<div class="faq-container" >
  <content-head title="FAQ" sub-title="live" class="content-head" />
  <div class="container-banner">
    <div v-for="item in list" class="accordions-container"  >
      <accordion class="accordions" :item="item" :key="item" />
    </div>
  </div>

</div>
</template>

<script>

import Accordion from "./accordion";
import accordionList from '../../constants/accordion'
import ContentHead from "../contentHead/content-head";
export default {
  name: "accordionMainCase",
  components: {ContentHead, Accordion},
  data(){
    return{
      list:null
    }
  },
  mounted() {
    this.list=accordionList
  }


}
</script>

<style scoped>
.faq-container{
  width: 100%;

  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
}
.content-head{
  width: 85%;
}
.container-banner{

  height: auto;

  display:flex;
  flex-flow: wrap;
  justify-content: center;
 gap: 10px;


}

.accordions{

}

</style>
