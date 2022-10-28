<template>
<div class="ib-button">

  <button  @click="confirm" class="btn" :class="[roundedClass,outlinedClass]"
          :style="{ 'background-color': bgColor }" >

    <ib-icon  v-if="direction ==='left'" :icon="Icon" />
    <span  :style="{ 'color': textColor ,'margin-left':margin}"  > {{text}}</span>
    <ib-icon  v-if="direction==='right'"  :icon="Icon" />

  </button>

</div>
</template>

<script>
import IbIcon from "../icon/ib-icon";
export default {
  name: "ib-button",
  components: {IbIcon},
  props:{
    direction:{
      required:false,
      type:String,

    },
    round:{
      type:Boolean,
      default:false,
      required:false

    },
    outlined:{
      type:Boolean,
      default:false,
      required:false
    },
    padding:{
      type:String,
      required:false,
      default:null,
    },
    text:{
      type:[String,Number],
      default:null,
      required:false

    },
    bgColor:{
      type:String,
      default:null,
      required:false
    },
    textColor:{
      type:String,
      default:null,
      required:false
    },
    Icon:{
      required:false,
      type:String,

    },
    margin:{
      type:String,
      required:false
    },

  },

  data(){
    return{
      button:'buttons'
    }
  },
  methods:{
    confirm(e){
      this.$emit("clicked",'ugur')
      console.log(e)
    }
  },

  computed:{
    roundedClass(){
       return this.round ? 'round-class' :null
    },

    outlinedClass(){
      return this.outlined ? 'outlined-class' :null
    }
  },

}
</script>

<style lang="scss">

.ib-button{

  .btn{
    display: flex;
    justify-content: space-between;
    background-color: transparent;
    outline: none;
    border: none;
  }

  .round-class{
    border-radius: 1000px;
    padding: 11px 24px;
  }

  .outlined-class{
    border: 1px solid #B4975A;
    padding: 11px 24px;
  }
  .paddings{
    padding: 11px 24px;
  }

}
</style>
