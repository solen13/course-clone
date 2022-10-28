<template>
<div >
<template v-for="item in list" >
  <accordion class="accordions" :item="item" :key="item" />
</template>


</div>
</template>

<script>

import Accordion from "./accordion";
import accordionList from '../../constants/accordion'
export default {
  name: "accordionMainCase",
  components: {Accordion},
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

</style>
