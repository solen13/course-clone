<template >

  <div class="live-corese-Content">



    <div class="card-banner">


  <content-head title="Our course"  sub-title="Here some descriptions..." :click="btnClick" :buttonview=btnText />


      <div class="card-contener">
        <div class="card-content" v-for="item in all" :key="item">
          <img src="../../static/cardImage.png" alt="">

          <div class="contents">
            <P>Until 31 April 2020</P>
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
  margin-bottom: 24px;

  .card-banner{
    width: 1180px;
    height: auto;
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
      .card-content:first-child{
        margin-left: 0;
      }
    }
  }

}

</style>

