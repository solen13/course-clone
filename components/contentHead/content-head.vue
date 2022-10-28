<template>
  <div class="card-head">

        <span>
           <h1>{{title}}</h1>
           <h2>{{ subTitle }}.</h2>
        </span>
    <ib-button text-color="#2D2B74" :text=buttonview :round="true" bg-color="#EBEEF3"  />

  </div>

</template>

<script>
export default {
  name: "content-head",
  props:{

   title:{
     type:String,
     required:false,
     default:null
   },
    subTitle:{
      type:String,
      required:false,
      default:null
    },
    buttonview:{

      required:false,
      default:'View All'
    },
   buttonClose: {

      required:false,
      default:'Close'
    },
    rount:{
     default:true
    }

  }
}
</script>

<style lang="scss" scoped>
.card-head{
  display: flex;
  justify-content: space-between;
  span{
    margin-bottom: 24px;
    h1{
      font-size: 24px;
      color: #425466;
      margin-bottom: 8px;
    }
    h2{
      font-size: 16px;
      color: #6C7C8C;
    }

  }

}
</style>
