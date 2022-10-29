<template>
  <div class="sildebar">
    <ul>
      <li v-for="item in lists" :key="item">
        <nuxt-link class="nuxt-links" :to='item.url' active-class="active">
          <span>{{ item.title }}</span>
          <img src="../../static/icon/right.svg" alt="">
        </nuxt-link>

      </li>


    </ul>
  </div>
</template>

<script>
import questions from '../../constants/questions'

export default {
  name: "sliderQuestions",
  data(){
    return{
      lists:null
    }
  },
  mounted() {
    this.lists= questions

  }
}
</script>

<style lang="scss" scoped>
  .sildebar{
    width: 300px;
    height: 80vh;
    margin-left: 10px;

    border: 1px solid #EBEEF3;
    border-radius: 8px;
    padding: 20px;
    ul{
      li{
        display: flex;
        align-items: center;
        list-style: none;
        text-decoration: none;
        .nuxt-links{
          width: 300px;
          margin-bottom: 18px;
          padding: 11px;
          text-decoration: none;
          color: #6C7C8C;
          font-size: 18px;

          display: flex;
          justify-content: space-between;

        }
        .active{
          background-color: #F8F9FB;
          border-radius: 8px;
          padding-left: 15px;
          border: 1px solid #EBEEF3;
        }
        .nuxt-links:hover{
          background-color: #F8F9FB;
          border-radius: 8px;
          padding-left: 15px;
          border: 1px solid #EBEEF3;
        }
      }
    }
  }




</style>
