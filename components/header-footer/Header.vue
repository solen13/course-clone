<template>
  <div class="Header-Contener">

    <ul>

      <li>
        <img class="logo" src="../../static/Foundation.png" alt="">
      </li>

      <li>
        <ib-button margin="5px" icon="home"  direction="left"  text="HOME" text-color="#6C7C8C" @clicked='home' />
      </li>

      <li>
        <ib-button  margin="5px"  icon="icon3"  direction="left"  text="COURSES" text-color="#6C7C8C"  @clicked="courses" />
      </li>

      <li>
        <ib-button   margin="5px"  icon="icon4"  direction="left"  text="QUESTIONS" text-color="#6C7C8C" @clicked="question"  />
      </li>

      <li class="search">
        <input  type="search" placeholder="Search">



      </li>
      <li>
        <select>
          <option>TÜRKÇE</option>
          <option>ENGLISH</option>
        </select>
      </li>

      <li    class="regester-btn">
        <ib-button v-if="this.$store.state.login.loginButton" :round="true"  :outlined="true" text="Sing in" text-color="#B4975A" bgColor="#FFFFFF"  />

        <ib-button  v-if="this.$store.state.login.loginButton" :round="true"  text="register" text-color="#FFFFFF" bgColor="#2D2B74" @clicked="register"  />
        <ib-button v-else :round="true"  text="Profile" text-color="#FFFFFF" bgColor="#2D2B74"  @clicked="login"   />
      </li>

    </ul>

      <div>

      </div>





  </div>
</template>

<script>

import ibButton from "../button/ib-button";
export default {
  name: "Header",
  components:{
    ibButton
  },
  props:{
    data:String
  },
data(){
    return{
  toggle:null
    }
},

  methods:{
    register(){
       this.$store.commit('login/toggleModal',true)
    },
    login(){
      this.$router.push('/user/myProfileUpdate')
    },
    home(){
      this.$router.push('/')
    },
    question(){
      this.$router.push('/questions/privacy-policy')
    },
    courses(){
      this.$router.push('/courses')
    }

  },



}
</script>

<style lang="scss" scoped >

@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&family=Roboto:wght@100;400&display=swap');


$active_coffe:#B4975A;
$general_font_color:#6C7C8C;

$title_color:#425466;

$border_color:#EBEEF3;
$primary:#2D2B74;


*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  list-style: none;
  text-decoration: none;
  font-family: 'Inter', sans-serif;
}

.imgs{
  width:14.67px ;
  height: 13.1px;
  margin-right: 9px;
}
.Header-Contener{
  width: 100%;
  height: 88px;
  background-image: url("../../static/Right Image.png");
  background-repeat: no-repeat;
  background-position: left;

  display: flex;
  align-items: center;
  justify-content:center;

 ul{
   width: 83%;
   display: flex;
   align-items: center;
   justify-content: space-around;

   li{

     .logo{
       width: 116px;
       height: 72px;

     }

     select{
       padding: 11px 8px 11px 16px;
       border: 1px solid  $border_color;
       color: $general_font_color ;
       outline: none;
     }

   }
   .regester-btn{
     display: flex;

     button{
       padding: 11px 24px 11px 24px;
       margin-left: 5px;
     }
   }

   .search{
     input{
       width:302px ;
       height: 40px;
       outline: none;
       border: 1px solid $border_color ;
       color:$general_font_color  ;
       border-radius: 6px;
       padding: 10px 11px ;

     }
   }


 }



  }
</style>
