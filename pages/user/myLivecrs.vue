<template>
 <div class="livecourse">
   <h1>My Live Courses</h1>

    <span class="livecourse-btn">
      <button class="btn1" @click="onComming">On Comming</button>
      <button class="btn2 pasif" @click="past">Past</button>
    </span>

   <ul  v-if="active">
     <li>
       <h3>Devam eden kuslarınız</h3>
       <span class="date">
         <span>
           <p>WILL START AT</p>
           <p>29.10.2021 - 13:00 AM - 14:00 AM</p>
         </span>
         <ib-button text="View Courses" :round="true" :outlined="true" text-color="#B4975A" />
       </span>
     </li>
   </ul>


   <ul v-else>
     <li>
       <h3>Level 4</h3>
       <span class="date">
         <span>
           <p>WILL START AT</p>
           <p>29.10.2021 - 13:00 AM - 13:00 AM</p>
         </span>
         <ib-button text="View Courses" :round="true" :outlined="true" text-color="#B4975A" />
       </span>
     </li>
   </ul>

 </div>



</template>

<script>
import IbButton from "../../components/button/ib-button";
export default {
  name: "myLivecrs",
  components: {IbButton},

  data(){
    return{
      active:true
    }
  },

  methods:{
    onComming(){
      this.active= true
      let actives=document.querySelector('.btn1')
      let actives2=document.querySelector('.btn2')

      actives2.classList.add('pasif')
      actives.classList.remove('pasif')

    },
    past(){
     this.active =false
      let actives=document.querySelector('.btn1')
      let actives2=document.querySelector('.btn2')

      actives.classList.add('pasif')
      actives2.classList.remove('pasif')
    }
  }
}
</script>

<style lang="scss" scoped>
.livecourse{
  width: 100%;
  height: 400px;
  h1{
    color:#425466;
    font-size: 24px;
    margin-bottom: 24px;

  }
  .pasif{
    background-color: transparent !important;
    color:#6C7C8C !important;
    border: none !important;
  }
  .livecourse-btn{

    button{
      padding: 11px;

      border-radius: 8px;
      background-color: #F8F9FB;
      color:#B4975A;
      border: 1px solid #EBEEF3;
      margin-bottom: 24px;
    }

  }


  ul{

    li{
      width: 100%;
      height: 72px;
      padding-left: 24px;
      padding-right: 24px;
      display: flex;
      flex-flow: row;
      justify-content: space-between;
      align-items: center;
      background-color: #ffffff;
      border-radius: 8px;
      border: 1px solid #EBEEF3;
      h3{
        color: #425466;
      }
      .date{
        display: flex;
        flex-flow: row;

        span{
          margin-right: 15px;
          display: flex;
          flex-flow: column;
          p{
            color:#6C7C8C;
          }
          p:first-child{
            font-size:10px;
            align-self: flex-end;
            margin-bottom: 8px;
          }
        }
      }
    }
  }
}
</style>
