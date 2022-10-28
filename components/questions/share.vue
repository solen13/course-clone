<template>
<div class="share">
  <p>SHARE</p>
<ul>
  <li> <ib-button icon="sosyalIcon2" margin="10px" direction="left" text="Facebook" text-color="#3B5998" /> </li>
  <li> <ib-button icon="sosyalIcon3" margin="10px" direction="left" text="Twiter" text-color="#1DA1F2" /> </li>
  <li> <ib-button icon="sosyalIcon4" margin="10px" direction="left" text="Whatsapp" text-color="#128C7E" /> </li>
  <li> <ib-button icon="sosyalIcon5" margin="10px" direction="left" text="Telegram" text-color="#0088CC" /> </li>
  <li> <ib-button icon="sosyalIcon1" margin="10px" direction="left" text="Instegram" text-color="#5851DB" /> </li>
</ul>
</div>
</template>

<script>
import IbButton from "../button/ib-button";
export default {
  name: "share",
  components: {IbButton}
}
</script>

<style lang="scss" scoped>
  .share{
   width: 100%;

    p{
      color: #6C7C8C;
      font-size: 12px;
    margin-bottom: 20px;
      font-weight: 700;
    }
    ul{
      display: flex;
      list-style: none;
      gap:25px;
      li{

      }
    }
  }
</style>
