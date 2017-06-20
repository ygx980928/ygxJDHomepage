<template>
    <div class="jduser" id="jduser">
       <i class="user-a">
           <img src="../images/ren.png" width="30" height="30"/>
            <div class="user-aa">
                京东会员
            </div>
       </i>
       <i class="user-b">
           <img src="../images/gouwuch.png" width="20" height="20" style="margin-left: 5px;margin-top: 5px"  />
           <div class="user-bb">
               购物车
           </div>
       </i>
       <i class="user-c">
           <img src="../images/xin.png" width="25" height="25" style="margin-top: 5px;margin-left: 5px">
           <div class="user-cc">
               特别关心
           </div>
       </i>
    </div>
</template>
<script>
  export default{
      data(){
          return{}
      },

  }
</script>
<style>
 .jduser{
     width: 35px;
     height: 300px;
     position: fixed;
     left: 0px;
     top:200px;
     z-index: 9999999;
 }
 .jduser i{
         display: inline-block;
         width: 35px;
         height: 35px;
         background: #7a6e6e;
         margin-top: 2px;
         position: relative;
 }
 .user-aa{
     width: 70px;
     height: 35px;
     background: red;
     color: #fff;
     position: absolute;
     left:-100px;
     top:0;
     font-size: 14px;
     text-align: center;
     line-height: 35px;
 }
 .user-bb{
     width: 70px;
     height: 35px;
     background: red;
     color: #fff;
     position: absolute;
     left:-100px;
     top:0;
     font-size: 14px;
     text-align: center;
     line-height: 35px;
 }
 .user-cc{
     width: 70px;
     height: 35px;
     background: red;
     color: #fff;
     position: absolute;
     left:-100px;
     top:0;
     font-size: 14px;
     text-align: center;
     line-height: 35px;
 }
 .user-a,.user-b,.user-cc:hover{
      transition:all 1s ease;
      background: red;

  }
 .user-a:hover .user-aa{
     transition:all 1s ease;
     left:35px;
     z-index: -1;
     border-radius: 0px 8px 8px 0px;
 }
 .user-b:hover .user-bb{
     transition:all 1s ease;
     left:35px;
     z-index: -1;
     border-radius: 0px 8px 8px 0px;
 }
 .user-c:hover .user-cc{
     transition:all 1s ease;
     left:35px;
     z-index: -1;
     border-radius: 0px 8px 8px 0px;
 }
</style>