<template>
 <nav id="nav" class="clearfix">
     <ul class="fl ul1">
         <li class="clearfix fr" >
             <i class="fl"></i><div class="fl bj">&nbsp;{{adr}}</div>
             <div class="address" v-show="true">
                 <ul class="ul2">
                     <li v-for="(item,index) in address" v-on:click="shwi(item,index)" :class="{'active':index==curIndex?!cl:cl}">{{item}}</li>
                 </ul>
             </div>
         </li>
     </ul>
     <!--地址-->
     <ul class="fr ul3">
         <li><a href="#" class="landing">你好,请登陆</a><a href="#" style="color: red;margin-left: 2px">     免费注册</a></li>
         <li style="width: 1px;height:10px;background:#ccc;margin: 11px 5px 0"></li>
         <li><a href="#">我的订单</a></li>
         <li style="width: 1px;height: 10px;background:#ccc;margin: 11px 5px 0"></li>
         <li class="myjd-a" style="position: relative;">
             <a href="#">我的京东</a>
             <i class="xjt" ></i>
             <!--myjd start-->
             <div class="myjd-b">
               <div class="fl myjd-c" v-for="item in myjd"><a href="#" style=" font-size: 12px;
        color:#989898;">{{item}}</a></div>
             </div>
             <!--myjd end-->
         </li>
         <li style="width: 1px;height: 10px;background:#ccc;margin: 11px 5px 0"></li>
         <li><a href="#">京东会员</a></li>
         <li style="width: 1px;height: 10px;background:#ccc;margin: 11px 5px 0"></li>
         <li><a href="#">企业采购</a></li>
         <li style="width: 1px;height: 10px;background:#ccc;margin: 11px 5px 0"></li>
         <li class="service"><a href="#">客户服务</a><i class="xjt" ></i>
              <div class="service-a">
                  <div  v-for="item in service" class="service-b"><a href="#" style=" font-size: 12px;
        color:#989898;">{{item}}</a></div>
              </div>
         </li>
         <li style="width: 1px;height: 10px;background:#ccc;margin: 11px 5px 0"></li>
         <li class="sng">
             <a href="#">网站导航</a><i class="xjt" ></i>
             <!--content-->
              <div class="sng-a">
                  <div class="sng-all sng-fist">
                     <dl>
                         <dt><b style="color: #000;margin-left: 20px">特色主题</b></dt>
                         <dd  class="fl tszt" v-for="item in tszt">{{item}}</dd>
                     </dl>
                  </div>
                  <div class="sng-all">
                      <dl>
                          <dt><b style="color: #000;margin-left: 20px">特色主题</b></dt>
                          <dd  class="fl tszt" v-for="item in tszt">{{item}}</dd>
                      </dl>
                  </div>
                  <div class="sng-all">
                      <dl>
                          <dt><b style="color: #000;margin-left: 20px">特色主题</b></dt>
                          <dd  class="fl tszt" v-for="item in tszt">{{item}}</dd>
                      </dl>
                  </div>
                  <div class="sng-all">
                      <dl>
                          <dt><b style="color: #000;margin-left: 20px">特色主题</b></dt>
                          <dd  class="fl tszt" v-for="item in tszt">{{item}}</dd>
                      </dl>
                  </div>
              </div>
             <!--content end-->
         </li>
         <li style="width: 1px;height: 10px;background:#ccc;margin: 11px 5px 0"></li>
         <!--手机京东-->
         <li style="position: relative" class="sjjd">
             <a href="#">手机京东</a>
             <i class="xjt" ></i>
             <img src="../images/Qrcode2.jpg" style="position: absolute;">
             <img class="Qrcode1" src="../images/Qrcode1.jpg" style="position: absolute">
         </li>
         <!--end-->
     </ul>
     <!--Right-->
 </nav>
</template>
<script>
    export default {
        name: 'nav',
        data () {
            return {
                cl:false,
                curIndex:0,
                adr:'北京',
                tszt:['发现好货','京东预售','京东金融','京东试用','全球售','优惠券','闪购','京东会员','秒杀','定期送','装机大师','新奇特企业','金融服务','礼品购','智能馆','0元评测','In货推荐','北京老字号','买什么'],
                service:[
                    '帮助中心',
                    '售后服务',
                    '在线客服',
                    '意见建议',
                    '电话客服',
                    '客服邮箱',
                    '金融咨询',
                    '售全球客服'
                ],
                myjd:['待处理订单',
                    '返修退换货',
                    '降价商品',
                    '消息',
                    '我的问答',
                    '我的关注',
                    '我的京豆',
                    '我的白条',
                    '我的优惠券',
                    '我的理财'],
                address:[
                    '北京','上海','天津','重庆','河北','山西','河南','辽宁','吉林','黑龙江','内蒙古','江苏','山东','安徽','浙江','福建','湖北','湖南','广东','广西','江西','四川','海南','贵州','云南','西藏','陕西','甘肃','青海','宁夏','新疆','港澳','台湾','钓鱼岛','海外'
                ]
            }
        },
        methods:{
            shwi(item,index){
//                console.log(index)
                this.adr=item
                this.curIndex = index
            }
        },
        components:{

        }
    }
</script>
<style>
    nav{
        width: 1190px;
        height: 30px;
        background: #ddd;
        z-index: 2231;
        border:none;
        font-size: 12px;
        color:#000;

    }
    .ul1{
        width: 257.56px;
        height: 30px;
    }
    .ul1>li{
        width: 57.56px;
        height: 100%;
        background: #ddd;
        position: relative;

    }
    .ul1>li:hover{
        background: #fff;
        z-index: 12;
    }
    .ul1 li:hover .address{
        display: block;
    }
    .ul1 li i{
        display: inline-block;
        width: 14px;
        height: 14px;
        background: #000;
        background:url("../images/Zuobiao.png" ) no-repeat;
        margin-top: 8px;
        margin-left: 2px;
    }
    
    .ul1 li .bj{
        height: 30px;
        line-height: 30px;
    }
    .address{
        width: 350px;
        height: 218px;
        background: #fff;
        position: absolute;
        left: 0;
        top: 30px;
        border: 1px solid #989898;
        border-top:none;
        display:none;
        z-index: 12;
    }
    .ul2 li{
        text-align: center;
        width: 60px;
        height: 28px;
        line-height: 24px;
        float: left;
        margin:0 5px 0 5px;
        cursor: pointer;
    }
    .active{
        background: red;
        color: #fff;
    }
    .ul3{
        width: 700px;
        height: 30px;
    }
    .ul3>li{
        float: left;
        line-height: 30px;
        margin-right: 8px;
        margin-left: 5px;
    }
    .ul3>li>a{
        font-size: 12px;
        color:#989898;
    }
    .ul3>li :hover{
        color: #c81623;
        z-index: 12;
    }
    .landing:hover{
        color:#c81623;
    }
    .xjt{
        width: 12px;
        height: 10px;
        background: url("../images/xia.png");
        display: inline-block;
        margin-left: 2px;
    }
     .myjd-a{
         position: relative;
         text-align: center;
         font-size: 12px;
         color:#000;
     }
    .myjd-a:hover{
        background: #fff;
    }
    .myjd-a:hover .myjd-b{
        display: block;
        border:1px solid #989898 ;
        border-top: none;
        z-index: 12;
    }
    .myjd-b{
        width: 282px;
        height: 163px;
        background: #fff;
        position: absolute;
        left:0;
        top:30px;
        display: none;
    }
    .myjd-c{
        width: 50%;
        height:30px;
    }
    .service-b{
        width: 50%;
        height:30px;
        float: left;
        text-align: center;
        z-index: 10;
    }
    .service{
        position: relative;
    }
    .service:hover{
        background: #fff;
    }
    .service-a{
        width: 238px;
        height: 120px;
        background: #fff;
        position: absolute;
        display: none;
        left: -176px;
    }
    .service:hover .service-a{
        display: block;
        border: 1px solid #989898;
        border-top: none;
        z-index: 12;
    }
    .sng{
        position: relative;
    }
    .sng:hover{
        background: #fff;
    }
    .sng:hover .sng-a{
        display: block;
        border:1px solid #989898;
        border-top: none;
    }
    .sng-a{
        position:absolute;
        width:1190px;
        height: 186px;
        /*border: 1px solid #000;*/
        left: -1030px;
        display: none;
        z-index: 12;
    }
    .sng-all{
        width: 296px;
        height: 186px;
        float: left;
        border-left: 1px dashed #ccc;
        background: #fff;
    }
    .sng-fist{
       border: none;
    }
    .tszt{
        width: 60px;
        line-height: 30px;
        height: 30px;
        margin-left: 10px;
        text-align: center;
        cursor: pointer;
        font-size: 12px;
        color:#989898;
    }
    .Qrcode1{
        position: absolute;
        left: -100px;
        top:30px;
        display: none;
    }
    .sjjd:hover .Qrcode1{
        display: block;
        border: 1px solid #989898;
        border-top:none;
        z-index: 12;
    }
</style>