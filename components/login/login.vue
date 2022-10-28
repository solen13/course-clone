<template>

  <div class="login">

    <p @click="exit">X</p>
    <h6> Sing up</h6>
    <input type="email" placeholder="Your mail">
    <input type="text" placeholder="Your name">
    <input type="password" placeholder="Your password">
    <button @click="logins"> Register</button>

    <span>

      <a href="#">Already have an account? </a>
      <a href="#"> Log in </a>

    </span>

  </div>

</template>

<script>
export default {
  name: "login",

methods:{
    exit(){

        this.$store.commit('login/toggleModal',false)
    },
  logins(){

    this.$store.commit('login/logiToggle',false)
    this.$store.commit('login/toggleModal',false)
  }
}
}
</script>

<style lang="scss" scoped>




.login{
  width: 100%;
  height: 100%;
  background-color: #ffffff;
  border-radius: 8px;
  display: flex;
  flex-flow: column;
  padding: 32px;
  position: relative;
  p{
   align-self: end;
    color: #0A2540;
    font-size: 16px;
    font-weight: 900;
    cursor: pointer;
    padding: 4px;
  }
  h6{
    font-size:24px;
    color: #425466;
    margin-bottom: 24px;
  }
  input{
  outline: none;
    border: 1px solid #EBEEF3;
    color: #425466;
    font-size:16px;
    margin-bottom: 32px;
    padding: 12px;
    border-radius: 8px;
  }
  button{
    background-color: #2D2B74;
    outline: none;
    border: none;
    color:#FFFFFF ;
    padding: 11px;
    border-radius: 1000px;
    margin-bottom: 32px;

  }
  span{
    align-self: center;
   a{
     text-decoration: none;
     color: #6C7C8C;
     font-size: 14px;
     margin-left: 16px;
   }
    a:last-child{
      color: #2D2B74;
    }
  }
}



</style>
