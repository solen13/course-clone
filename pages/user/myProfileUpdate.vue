<template>
  <div class="profile-update">
   <h2>Account Settings</h2>
    <from >

        <span>
          <p>Mail</p>
          <input value="mr.enesaktas@gmail.com" type="email">
        </span>

        <span>
          <p>Name</p>
          <input value="Enes Aktaş" type="text">
        </span>

        <span>
           <p>Password</p>
          <ib-button class="eye-btn" icon="eye" direction="left"  @clicked="hideShow"  />
           <input  v-if="showPassword" value="deeonfşdfnpı34" type="text" >
           <input v-else value="deeonfşdfnpı34" type="password">

        </span>

        <span>
          <input type="password" placeholder="Change Password">
        </span>

    </from>

    <ib-button text="update" :round="true" bg-color="#2D2B74" text-color="#FFFFFF"  />

  </div>

</template>

<script>
import IbButton from "../../components/button/ib-button";
export default {
  name: "profileDyazayn",
  components: {IbButton},
  data(){
    return{
      showPassword: false,
    }
  },

  layout:'profile',
  methods:{
    hideShow(){

      this.showPassword = !this.showPassword;
    }
  }
}
</script>

<style lang="scss" scoped>
.profile-update{
  width: 100%;
  height: 500px;
  display: flex;
  flex-flow: column;
  padding: 40px;
  position: relative;
  h2{
    color: #425466;
    font-size: 24px ;
    margin-bottom: 24px;
  }
  from{
    display: flex;
    flex-flow: column;
    span{
      position: relative;

      width: 343px;

      input{
        width: 100%;
        padding: 12px;
        color:#6C7C8C;
        font-size: 16px;
        margin-bottom: 32px;
        outline: none;
        border: 1px solid #EBEEF3;
        border-radius: 8px;
      }
      p{
        padding: 5px;
        position: absolute;
        margin-left: 10px;
        color: #425466;
        background-color: #FFFFFF;
        margin-top: -14px;
      }
      .eye-btn{
        position: absolute;
        right: 0;
        margin-top: 10px;
        margin-right: 5px;
      }
    }
  }

}
</style>
