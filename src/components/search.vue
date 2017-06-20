<template>
    <div class="search">
        <img class="log" src="../images/logo.gif"/>

            <input class="text" type="text"  :placeholder="inner"  style="color: #000">
            <button class="button"><i></i></button>
           <!--购物车 start-->
        <div class="cw-icon">
            <i></i>
           <span>我的购物车</span>
            <div class="gm">
                <img src="../images/58004d6dN2927f0f7.png"/>
                购物车中没有选购的商品
            </div>
        </div>
        <!--购物车end-->
        <!--val start-->
        <ul class="valb">
            <li class="fl val" v-for="item in val">{{item}}</li>
        </ul>
        <!--val end-->
        <div class="g-tit">
            <ul style="margin-right: 10px;">
                <li class="x-tit" v-for="item in tita">{{item}}</li>
                <li class="x-tita">|</li>
            </ul>
            <ul>
                <li class="x-tit" v-for="item in titb">{{item}}</li>
                <li class="x-tita">|</li>
            </ul>
            <ul>
                <li class="x-tit" v-for="item in titc">{{item}}</li>
            </ul>
        </div>
        <div class="ppa"></div>
    </div>
</template>
<script>
    export default{
        name:'search',
        data(){
            return{
                plho:'bbb',
                plhoa:['电脑主机IE7','温奶器','飞利浦空气精华器','洗衣机'],
                num:0,
                inner:'电脑主机IE7',
                val:[
                    '房产低价拍','手机专场','限时抢购','京东服装','1折购家电','围巾男','烤箱','食品饮料','蓝牙耳机'
                ],
                tita:[
                    '秒杀',
                    '优惠券',
                    '闪购',
                    '拍卖'
                ],
                titb:[
                    '服装城',
                    '京东超市',
                    '生鲜',
                    '全球购'
                ],
                titc:[
                    '京东金融   '
                ]
            }
        },
        methods:{
             plhoaa(){
                 var that = this;
                 setInterval(hah,4000)
                 function hah() {
                     that.inner = that.plhoa[that.num]
                     that.num++;
                     if(that.num>that.plhoa.length-1){
                         that.num=0
                     }
                 }
             }
        },
        mounted(){
            this.plhoaa()
    },
        components:{
        }
    }
</script>
<style>
    .search{
        width: 1190px;
        height: 140px;
        /*background: red;*/
        position: relative;
    }
    .log{
        margin-top: -30px;
    }
    .text{
        width: 500px;
        height: 34px;
        color: rgb(153, 153, 153);
        border:1px solid red;
        position: absolute;
        left: 47%;
        top:50%;
        margin-top: -34px;
        margin-left: -250px;
    }
    .button{
        width: 50px;
        height: 36px;
        cursor: pointer;
        background: #f10215;
        border: 1px solid #f10215;
        position: absolute;
        left:68%;
        margin-left: 2px;
        top:25%;
        margin-top: 1px;
    }
    button i{
        width: 20px;
        height: 20px;
        display: inline-block;
        background: url("../images/icon.png");
    }
    .cw-icon{
        width: 188px;
        height: 33px;
        border: 1px solid #ccc;
        position: absolute;
        right: 88px;
        top:37px;
        text-align: center;
        line-height: 40px;
        color: red;
        font-size: 15px;
    }
    .cw-icon i{
        width: 16px;
        height: 16px;
        background: url("../images/car.png");
        display: inline-block;
        margin-left: -70px;
    }
    .cw-icon span{
        color: red;
        position: absolute;
        left:70px;
        top:-3px;
        font-size: 14px;
    }
    .cw-icon:hover{
        border-bottom:none;
        z-index: 12;
    }
    .cw-icon:hover .gm{
        display: block;
    }
   .gm{
       width: 308px;
       height:69px;
       position: absolute;
       left:-120px;
       top:32px;
       border: 1px solid #ccc;
       line-height: 69px;
       display: none;
       background: #fff;
       color:#ccc;
   }
    .gm img{
        margin-top: 10px;
    }
    .valb{
        position: absolute;
        left:350px;
        top:80px;
        cursor: pointer;
    }
    .val{
        margin-right: 10px;
    }
    .val:hover{
        color: red;
    }
    .g-tit{
        width: 790px;
        height: 40px;
        /*background: red;*/
        position: absolute;
        left:200px;
        bottom: 0;
    }
    .x-tita{
        float: left;
        height: 40px;
        line-height: 40px;
        margin:0 20px 0 0;
        color: #555;
    }
    .x-tit{
        float: left;
        height: 40px;
        font-weight: 700;
        font-size: 16px;
        line-height: 40px;
        margin:0 30px 0 0;
        color: #555;
        cursor: pointer;
    }
    .x-tit:hover{
        color: #f10215;
    }
    .ppa{
        width: 190px;
        height:40px;
        background: url("../images/pinpai-a.gif");
        position: absolute;
        right:0;
        bottom:0;
    }
</style>