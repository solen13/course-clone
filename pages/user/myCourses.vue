<template>
  <div class="myCourses">
   <h3> My Courses </h3>

    <ul>

      <li v-for="item in coursesList" :key="item">
        <h5>{{ item.title }}</h5>

       <span class="right">

         <span>
           <p>You’re started at</p>
           <p>{{ item.date }}</p>
         </span>

         <div class="proges-bar">
           <span class="proges">{{item.proges}}</span>

           <Counterounter
             size="2rem" active-stroke="#31BC81"
             :dash-count="100"
             :stroke-width="25"
             :dash-spacing="0"
             :active-count=item.proges
           />



         </div>

          <ib-button :outlined="true" text="View Course" text-color="#B4975A":round="true" />

      </span>

      </li>

    </ul>

  </div>
</template>

<script>
import IbButton from "../../components/button/ib-button";
import Counterounter from "../../components/progesBar/CircleCounter";
import constants from '../../constants/coursesList'
export default {
  name: "myCorse",
  components: {IbButton,Counterounter},


  data(){
    return{
      coursesList:constants
    }
  }

}
</script>

<style  lang="scss" scoped>
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
.myCourses{
  width:100% ;
  height: 400px;
  background-color: #90be3c;
  padding: 40px;

  h3{
    color: #425466;
    font-size:24px;
    margin-bottom: 24px;
  }
 ul{
   li{
     background-color: #F8F9FB;
     width: 100%;
     height: 72px;
     display: flex;
     justify-content: space-between;
     border-radius: 8px;
     align-items: center;
     padding-left: 24px;
     padding-right: 24px;
     border: 1px solid #EBEEF3;
     margin-bottom: 24px;
     h5{
       color: #425466;
       font-size: 16px;
     }
     .right{
       display: flex;
       align-items: center;
       span{
         margin-right:16px ;
         color: #6C7C8C;
         p:first-child{
           margin-bottom: 5px;
           font-size: 10px;
         }


       }
       .proges-bar{
         margin-right:16px ;
         position: relative;
         span{
           position: absolute;
           font-size: 12px;
           margin-left: 10px;
           margin-top: 10px;
         }
       }
     }

   }
 }

}
</style>
