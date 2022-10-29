<template>
<div class="left-banner">

 <span >
<p>Welcome</p>
   <h3>Enes Aktaş</h3>
 </span>

  <ul>
    <li v-for="item in profile"  :key="item">
      <nuxt-link  class="nuxtlink" :to="item.url" active-class="active">
       <div class="titles"> {{ item.title }}</div>
        <img src="../../static/icon/right.svg" alt="">
     </nuxt-link>

    </li>

  </ul>


</div>
</template>

<script>
import IbButton from "../button/ib-button";
import IbIcon from "../icon/ib-icon";
import profileLists from '../../constants/profileList'
export default {
  name: "leftComment",
  components: {IbIcon, IbButton},
  data(){
    return{
  profile:null
    }
  },
  mounted() {
   this.profile= profileLists

  }

}
</script>

<style lang="scss" scoped>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  text-decoration: none;
  list-style: none;
}
.left-banner{
  width:280px ;
  height:371px;
  background-color: #FFFFFF;
  border-radius: 8px;
 display: flex;
  flex-flow: column;
 align-items: center;
  border: 1px solid #EBEEF3;

  span{
    width: 100%;
    background-color: #F8F9FB;
    padding: 24px;
    border-bottom: 1px solid #EBEEF3;
    border-top-right-radius: 8px;
    border-top-left-radius: 8px;
    p{
      color: #6C7C8C;
      font-size: 12px;
      font-weight: 400;
      margin-bottom: 8px;
    }
    h2{
      color: #425466;
      font-size: 16px;
      font-weight: 600;
    }
  }
  ul{
    padding: 24px;
    width: 100%;
    height: auto;

    li{


       width: 100%;
      display:flex ;

      .nuxtlink{
        display: flex;
        justify-content: space-between;
        padding:11px;
        width: 100%;
        margin-bottom: 8px;

        .titles{
          color: #6C7C8C;
          font-size: 14px;
          font-weight: 400;
          background-color:transparent;
        }
        img{
          align-self: flex-end;
        }

      }

      .active{
        background-color: #F8F9FB;
        border-radius: 8px;
        padding-left: 15px;
        border: 1px solid #EBEEF3;
      }
      .nuxtlink:hover{
        background-color: #F8F9FB;
        border-radius: 8px;
        padding-left: 15px;
        border: 1px solid #EBEEF3;
      }
    }
  }

}

</style>
