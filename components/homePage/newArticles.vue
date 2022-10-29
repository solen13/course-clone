<template >

  <div class="live-corese-Content">



    <div class="card-banner">

   <content-head title="New & Articles"  sub-title="Here some descriptions..." :click="btnClick" :buttonview=btnText />

      <div class="card-contener">
        <div class="card-content" v-for="item in all" :key="item">
          <img src="../../static/cardImage.png" alt="">

          <div class="contents">
            <P>Until 31 may 2021</P>
            <h1>Article Title</h1>
            <p class="lang">What is the religion that is practiced by 1.6 billion people around the world?</p>

            <ib-button text-color="#B4975A"  text="View Course" :outlined="true" :round="true"  />

          </div>

        </div>
      </div>

    </div>


  </div>



</template>

<script>
import IbButton from "../button/ib-button";
import ContentHead from "../contentHead/content-head";
export default {
  name: "outCourse",
  components: {ContentHead, IbButton},
  data(){
    return{
      all:4,
      btnText:'View',
      isExpand:true,
    }
  },
  methods:{
    alls(){
      alert()
    },
    btnClick(){
      this.isExpand = !this.isExpand
      if(this.isExpand===true){
        this.btnText='view'
        this.all=4
      }
      else {
        this.btnText='close'
        this.all=8
      }
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

