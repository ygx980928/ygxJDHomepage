<template>
    <div id="ald">
        <div class="appa">
            <div class="bar"></div>
            <div  class="cat" style="overflow: scroll">
                <div id="tit_p" style="font-size: 16px"><span>618全民年中购物节</span></div>
                <div class="tit_pp"></div>
                <div class="cat_ga">
                    <img src="../images/ck3c.jpg" width="100%" height="100%">
                </div>
                <div class="cat_gb" >
                    <img src="../images/618xue.jpg" width="100%" height="100%">
                </div>
                <!--1-->
                <div style="text-align: center" class="cat_gc">
                    <img src="../images/591d4328N311aadc5.jpg" v-on:click="show = !show" >
                    <!--动画 START-->
                    <transition name="gqjy">
                        <div class="yunyan" v-if="show">
                            <div class="lb_a fl" v-for="item in phpoe">{{item}}</div>
                        </div>
                    </transition>

                    <!--动画 END-->
                </div>
                <!--1-->
                <!--2-->
                <div style="text-align: center" class="cat_gc">
                    <img src="../images/591d4310N93b7003d.jpg" v-on:click="showa = !showa" >
                    <!--动画 START-->
                    <transition name="gqjya">
                        <div class="yunyan" v-if="showa">
                            <div class="lb_a fl" v-for="item in phpoe">{{item}}</div>
                        </div>
                    </transition>

                    <!--动画 END-->
                </div>
                <!--2-->
                <!--3-->
                <div style="text-align: center" class="cat_gc">
                    <img src="../images/591d4306Ne55ee4d6.jpg" v-on:click="showb = !showb" >
                    <!--动画 START-->
                    <transition name="gqjyb">
                        <div class="yunyan" v-if="showb">
                            <div class="lb_a fl" v-for="item in phpoe">{{item}}</div>
                        </div>
                    </transition>

                    <!--动画 END-->
                </div>
                <!--3-->
                <div style="text-align: center" class="cat_gc">
                    <img src="../images/59118f62Nedc8300f.png" v-on:click="showd = !showd">
                    <transition name="gqjyc">
                        <img v-if="showd" src="../images/580ed76bNa79c108b.png">
                    </transition>
                </div>
            </div>
        </div>

    </div>
</template>
<script>
    export default{
        name:'adl',
        data(){
             return{
               phpoe:['爆品手机','电脑办公','潮流数码','图书音响','生活旅行','企业采购'],
               show:false,
               showa:false,
               showb:false,
                showd:false,
                hid:true,
             }
        }
    }
</script>
<style>
 .appa{
     color:rgb(94, 80, 80);
     position: fixed;
     right: -274px;
     top:20px;
     z-index: 99999;
     height: 100%;
     cursor: pointer;
     transition: all 1s ease;
 }
 .bar{
     width: 57px;
     height:160px;
     background: url("../images/bar618.png");
     position: absolute;
     left: -56.9px;
 }
 .cat{
     width: 270px;
     height: 100%;
     background: #333;
     float: left;
     position: relative;

 }
 #tit_p{
     width: 100%;
     height:40px;
     position: absolute;
     left:0;
     top:0;
     background: #eceaea;
     line-height: 40px;
    text-indent: 2em;
     font-size: 1.17em;
     font-weight: normal;
     color: #666;
 }
.tit_pp{
    width: 100%;
    height:40px;
}
.cat_ga{
    width: 100%;
    height: 197px;
    cursor: pointer;

}
.cat_gb{
    width: 100%;
    height: 45px;
   cursor: pointer;
    margin-top:2px;
}
.cat_gc{
    margin-top:2px;
}
 .yunyan{
     width: 100%;
     height: 60px;
     margin: 0 10px 0 10px;
     margin-top: 5px;
     border: 1px solid #000;
     opacity: 1;

 }
 /*.cat_gc:hover .yunyan{*/
     /*display: block;*/
 /*}*/
 .lb_a{
     width: 32%;
     height:27px;
     text-align: center;
     line-height: 27px;
     color: #abe0ff;
     font-weight: bold;
     font-size: 12px;
     border: 1px solid #000;
     cursor: pointer;

 }
 .gqjy-enter-active, .gqjy-leave-active {
     transition: opacity 1s
 }
 .gqjy-enter, .gqjy-leave-active {
     opacity:0
 }
 .gqjya-enter-active, .gqjya-leave-active {
     transition: opacity 1s
 }
 .gqjya-enter, .gqjya-leave-active {
     opacity:0
 }
 .gqjyb-enter-active, .gqjyb-leave-active {
     transition: opacity 1s
 }
 .gqjyb-enter, .gqjyb-leave-active {
     opacity:0
 }
 .gqjyc-enter-active, .gqjyc-leave-active {
     transition: opacity 1s
 }
 .gqjyc-enter, .gqjyc-leave-active {
     opacity:0
 }

  .appa:hover{
      transition: all 1s ease;
      right: 0px;
  }
</style>