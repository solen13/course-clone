<template>

  <div class="comment-contener">

   <div class="banner-left">

     <ul>
       <li v-for="item in 3" :key="item.id">

         <img src="@/static/resim.png" alt="">

         <span>
           <h1> John Doe</h1>
           <h3>24- Sales Manager</h3>
         </span>

       </li>
     </ul>

   </div>

    <div class="banner-right">

      <h1>It was a great experience</h1>
      <p>Lorem Ipsum is simply dummy text of the printing and typesettin
        g industry. Lorem Ipsum has been the industry's standard dummy text ev
        er since the 1500s, when an unknown printer took a galley of type and sc
        rambled it to make a type specimen book. It has survived not only five c
        enturies, but also the leap into electronic typesetting, remainin
        g essentially unchanged. <br><br>

        It was popularised in the 1960s with the release of Letraset sheets co
        ntaining Lorem Ipsum passages, and more recently with desktop publishing
        software like Aldus PageMaker including versions of Lorem Ipsum.
      </p>

    </div>

  </div>

</template>

<script>
export default {
  name: "comment"
}
</script>

<style lang="scss" scoped>
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
.comment-contener{
  width:100%;
  height: 428px;
  background-color:#EBEEF3 ;
   display: flex;
   padding-top:58px ;
  padding-left: 120px;
  padding-right: 230px;
  .banner-left{

    ul{

      display: flex;
      flex-flow: column;
     li{
       width: 280px;
       height:86px ;
       border-radius: 8px;
       background-color:#FFFFFF ;
       margin-bottom: 24px;
       list-style: none;
       display: flex;
       align-items: center;


       img{
         width: 40px;
         height: 40px;
         border-radius: 100%;
         margin-left: 16px;

       }
       span{
         margin-left: 16px ;
          H1{
            font-size: 14px;
            color: #425466;
            margin-bottom: 4px;
          }
          h3{
            font-size:14px ;
            color: #6C7C8C;
          }

       }

     }
    }
  }

  .banner-right{
    margin-left: 120px ;
    h1{
      color:#425466;
      font-size: 32px;
      margin-bottom: 32px;
    }
    p{

      color: #6C7C8C;
      font-size: 16px;
    }
  }
}

</style>
