<template >

  <div class="accordion-content">

    <div class="card-banner">

      <div class="card-container">

        <div class="card-content"  >
         <span class="head" >

           <span>
              <h3>{{item && item.title }}</h3>
              <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry.</p>
           </span>

           <ib-button icon="Vector" direction="left" :round="true" bg-color="#EBEEF3"  @clicked="toggleExpand()" />

         </span>

          <div :class="isExpand?'show' : 'hide' " class="accordion " >

            <ul>
              <li>{{item && item.content}}</li>
            </ul>

          </div>
        </div>

      </div>

    </div>

  </div>

</template>

<script>
import IbButton from "../button/ib-button";

export default {
  name: "accardion",
  components: {IbButton},
  props:{
    item:{
      type:Object,
      default: () => {},
    }
  },
  data() {
    return {
      veri: null,
      isExpand:false,
    }

  },

  created() {
    this.veri =this.items

  },
  methods: {
    toggleExpand(){

this.isExpand = !this.isExpand

    },
  }

}
</script>

<style lang="scss" scoped>

.accordion-content {
  width: 100%;
  height: auto;
  display: flex;
  justify-content: center;
  align-items: flex-start;
  .card-banner {
    width: 1180px;
    height: auto;

    .card-head {
      display: flex;
      justify-content: space-between;

      span {
        margin-bottom: 24px;

        h1 {
          font-size: 24px;
          color: #425466;
          margin-bottom: 8px;
        }

        h2 {
          font-size: 16px;
          color: #6C7C8C;
        }

      }

    }


    .card-container {

      display: flex;
      flex-wrap: wrap;
      justify-content: space-around;
      .card-content {
        width: 580px;
        height: auto;
        border: 1px solid #EBEEF3;
        border-radius: 8px;
        margin-bottom:20px ;
        padding: 24px;
        position: relative;

        .head{
          display: flex;
          margin-bottom: 20px;
         span{
           h3{
             color: #425466;
             font-size: 16px;
             margin-bottom: 8px;
           }
           p{
             width: 472px;
             color: #6C7C8C;
           }

         }
          button{
            border-radius: 100%;
            width: 30px;
            height: 30px;
            border: none;
          }
        }


        .accordion{
         border-top-left-radius: 50px;
         border-top-right-radius: 50px;
          width: 100%;
          height: 150px;
          background-color: rgba(108, 124, 140, 0.84);
        }
        .show{
         display: block;
        }
        .hide {
          display: none;
        }      }


    }
  }
}

</style>

