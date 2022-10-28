<template >

  <div class="live-corese-Content">



    <div class="card-banner">

      <div class="card-head">

        <span>
           <h1>News & Articles</h1>
           <h2>Here some descriptions...</h2>
        </span>

        <ib-button text-color="#2D2B74" v-if="all===4" text="view All" :round="true" bg-color="#EBEEF3" @clicked="all=8" />
        <ib-button text-color="#2D2B74" v-else text="Close" :round="true" bg-color="#EBEEF3" @clicked="all=4" />

      </div>


      <div class="card-contener">
        <div class="card-content" v-for="item in all" :key="item">
          <img src="@/static/cardImage.png" alt="">

          <div class="contents">
            <P>Until 31 may 2021</P>
            <h1>Article Title</h1>
            <p class="lang">What is the religion that is practiced by 1.6 billion people around the world?</p>

            <ib-button text-color="#2D2B74"  text="view Al" :round="true" bg-color="#EBEEF3" @clicked="alls" />

          </div>
        </div>
      </div>

    </div>


  </div>



</template>

<script>
import IbButton from "../button/ib-button";
export default {
  name: "outCourse",
  components: {IbButton},
  data(){
    return{
      all:4
    }
  },
  methods:{
    alls(){
      alert()
    }
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

  height: auto;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 10px;
  margin-bottom: 15px;
  height: auto;
  .card-banner{
    width: 1180px;


    .card-head{
      display: flex;
      justify-content: space-between;
      span{
        margin-bottom: 24px;
        h1{
          font-size: 24px;
          color: #425466;
          margin-bottom: 8px;
        }
        h2{
          font-size: 16px;
          color: #6C7C8C;
        }

      }

    }


    .card-contener{
      display: flex;
      flex-flow: wrap;
      height: auto;
       gap: 10px;
      .card-content{
        width: 280px ;
        height: 382px;
        border:1px solid #EBEEF3;
        display: flex;
        flex-flow: column;

        border-radius: 8px;

        img{
          width: 280px;
          height: 150px;
          margin-bottom: 24px;
        }


        .contents{
          width: 280px;
          display: flex;
          flex-flow: column;
          margin-left: 24px;
          p{
            font-size: 10px;
            color: #6C7C8C;
            margin-bottom: 16px;
          }
          h1{
            font-size: 16px;
            color:#425466;
            margin-bottom: 8px ;
          }
          .lang{
            color:#6C7C8C ;
            font-size:14px ;
            width: 232px;
          }


        }
        .corse-btn{
          align-self: flex-start;
        }

      }
      .card-content:first-child{
        margin-left: 0;
      }
    }
  }

}

</style>

