<template >

  <div class="live-corese-Content">
    <div class="card-banner">

     <content-head title="Live Course"  sub-title="Here some descriptions..."  />

      <div class="card-contener">
        <div class="card-content" v-for="item in all" :key="item">

          <img src="@/static/image.png" alt="">

          <div class="contents">
            <h1>Level1</h1>

            <ul>
              <li>What’s Islam?</li>
              <li>  The 5 Pillars of Islam </li>
              <li> The 6 Pillars of Faith  </li>
              <li> Story of Prophet Muhammed  </li>

            </ul>
            <ib-button  class="corse-btn" :round="true" text="View course" :outlined="true"  text-color="#B4975A" />

          </div>

        </div>

      </div>

    </div>

  </div>

</template>

<script>

import ContentHead from "../contentHead/content-head";
export default {
  name: "Live-corse",
  components: {ContentHead},
  data(){
    return {
      all:3
    }
  },
  methods:{

  }

}
</script>

<style lang="scss" scoped>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.live-corese-Content{
  width: 100%;
  height:auto;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 40px;
  margin-bottom: 40px;
  .card-banner{
    width: 1180px;
    height: auto;


    .card-contener{
      border: 1px solid #EBEEF3;
      border-radius: 10px;
      display: flex;
      flex-flow: wrap;
      .card-content{
        width: 392px ;
        height: 418px;
        border-right:1px solid #EBEEF3;
        display: flex;
        flex-flow: column;
        padding: 40px;
        img{
          width: 300px;
          height: 150px;
          margin-bottom: 24px;
        }


        .contents{
          width: 300px;
          display: flex;
          flex-flow: column;
          h1{
            font-size: 16px;
            color:#425466;
            margin-bottom: 8px ;
          }
          ul{
            margin-left: 19px;
            margin-bottom: 24px ;
            li{
              font-size: 14px;
              color:#6C7C8C;
            }

          }

        }
        .corse-btn{
          align-self: flex-start;
        }

      }
      .card-content:last-child{
        border: none;
      }
    }
  }

}

</style>
