<template>
<div class="selection">
   <h2>Choose day</h2>
  <ul class="container">

    <li class="card-content" v-for="item in list" :key="item" >

      <ul class="card-banner">

        <li class="date-title">{{ item.date }}</li>

        <li v-for="hour in item.hour" :key="hour" class="hour-btn">
          <span>{{ hour }}</span>
          <ib-button text="join" bg-color="#EBEEF3" text-color="#2D2B74" :round="true" @clicked="join"/>
        </li>

      </ul>

    </li>

  </ul>

</div>
</template>

<script>
import IbButton from "../../button/ib-button";
import lists from "../../../constants/chooseDay"
export default {
  name: "courseSelection",
  components: {IbButton},
  data(){
    return{
      list:null
    }
  },

  props:{
    item:{
      type:Object,
      default: () => {},
    }
  },
  methods:{
    join(){
      this.$router.push("/courses/selection/courses-detail")
    }
  },
  mounted() {
    this.list=lists
  }
}
</script>

<style lang="scss" scoped>
.selection{
  width:880px;
  height: auto;
  padding: 40px;
  background: #FFFFFF;
  border: 1px solid #EBEEF3;
  border-radius: 8px;
  list-style: none;
  .card-content{
    border: 1px solid #EBEEF3;
    list-style: none;
    margin-bottom: 10px;
    border-radius: 8px;
    .card-banner{
      list-style: none;

      .date-title{
        width: 100%;
        padding: 9px;
        font-weight: 500;
        font-size: 12px;
        background-color: #F8F9FB;
        border-bottom: 1px solid #EBEEF3;
        color: #425466;
        border-top-right-radius: 8px;
        border-top-left-radius: 8px;
      }
      .hour-btn{
        display: flex;
        align-items: center;
        justify-content: space-between;
        color: #425466;
        font-size: 16px;
        padding: 24px;
        border-bottom:1px solid #EBEEF3 ;
      }
      .hour-btn:last-child{
        border: none;
      }
    }
  }
}
</style>
