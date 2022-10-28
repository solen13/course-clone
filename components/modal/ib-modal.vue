<template>
  <div v-if="isShowModal" class="ib-modal">

    <div class="modal-content">

      <slot/>
    </div>

  </div>
</template>

<script>
export default {
  name: "ib-modal",
  methods:{
    closeModal(){
      this.$store.commit('login/toggleModal',false)
    }
  },
  computed:{
    isShowModal(){
      return this.$store.state.login.showModal
    }
  }
}
</script>

<style scoped>
.ib-modal {

  position: fixed; /* Stay in place */
  z-index: 1; /* Sit on top */
  left: 0;
  top: 0;
  width: 100%; /* Full width */
  height: 100vh; /* Full height */
  overflow: auto; /* Enable scroll if needed */
  background-color: rgb(0,0,0); /* Fallback color */
  background-color: rgba(0,0,0,0.4); /* Black w/ opacity */
  display: flex;
  align-items: center;
  justify-content: center;
}

/* Modal Content/Box */
.modal-content {
  height: 470px;
  width: 407px;

}
.close {
  color: #aaa;
  float: right;
  font-size: 28px;
  font-weight: bold;
}

.close:hover,
.close:focus {
  color: black;
  text-decoration: none;
  cursor: pointer;
}
</style>
