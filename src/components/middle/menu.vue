<template>
    <div id="menu" class="menus">
         <ul class="fcate_menu">
             <li class="cate_a cate_menu" >
                 <span>
                     家用电器
                 </span>
                 <div class="loyou l_a">
                     这是家用电器
                 </div>
             </li>
             <li class="cate_menu cate_b">
                 <span>手机</span>
                 <i>/</i>
                 <span>运营商</span>
                 <i>/</i>
                 <span>数码</span>
                 <div class="loyou l_b">
                    这是数码产品
                 </div>
             </li>
             <li class="cate_menu cate_c">
                 <span>电脑</span>
                 <i>/</i>
                 <span>办公</span>
                 <div class="loyou l_c">
                     这是电脑
                 </div>
             </li>
             <li class="cate_menu cate_d">
                 <span>家具</span>
                 <i>/</i>
                 <span>家居</span>
                 <i>/</i>
                 <span>家装</span>
                 <i>/</i>
                 <span>厨具</span>
                 <div class="loyou l_d">
                     这是家居
                 </div>
             </li>
             <li class="cate_menu cate_e">
                 <span>男装</span>
                 <i>/</i>
                 <span>女装</span>
                 <i>/</i>
                 <span>童装</span>
                 <i>/</i>
                 <span>内衣</span>
                 <div class="loyou l_e">
                  这是衣服
                 </div>
             </li>
             <li class="cate_menu cate_f">
                 <span>美状个户</span>
                 <i>/</i>
                 <span>宠物</span>
                 <div class="loyou l_f">
                     这是宠物
                 </div>
             </li>
             <li class="cate_menu cate_g">
                 <span>女鞋</span>
                 <i>/</i>
                 <span>箱包</span>
                 <i>/</i>
                 <span>钟表</span>
                 <i>/</i>
                 <span>宝珠</span>
                 <div class="loyou l_g">
                     这是珠宝
                 </div>
             </li>
             <li class="cate_menu cate-h">
                 <span>男鞋</span>
                 <i>/</i>
                 <span>运动</span>
                 <i>/</i>
                 <span>户外</span>
                 <div class="loyou l_h">
                     这是男鞋
                 </div>
             </li>
             <li class="cate_menu cate_i">
                 <span>汽车</span>
                 <i>/</i>
                 <span>汽车用品</span>
                 <div class="loyou l_i">
                     这是汽车
                 </div>
             </li>
             <li class="cate_menu cate_j">
                 <span>母婴</span>
                 <i>/</i>
                 <span>玩具乐器</span>
                 <div class="loyou l_j">
                     这是母婴
                 </div>
             </li>
             <li class="cate_menu cate_k">
                 <span>食品</span>
                 <i>/</i>
                 <span>酒类</span>
                  <i>/</i>
                 <span>生鲜</span>
                  <i>/</i>
                 <span>特产</span>
                 <div class="loyou l_k">
                     这是食品
                 </div>
             </li>
             <li class="cate_menu cate_l">
                 <span>礼品鲜花</span>
                 <i>/</i>
                 <span>农资绿植</span>
                 <div class="loyou l_l">
                     这是鲜花
                 </div>
             </li>
         </ul>

        <!--<div class="loyou "></div>-->
        <!--<div class="loyou"></div>-->
        <!--<div class="loyou"></div>-->
        <!--<div class="loyou"></div>-->
        <!--<div class="loyou"></div>-->
    </div>
</template>
<script>
    export default{
        name:'menu',
        data(){
            return{
               eletric:'家用电器',
                php:['手机','运营商']
            }
        },
        methods:{
              enter:function () {
                  alert(1)
              },
              leave:function () {
                  alert(2)
              }
        }

    }
</script>
<style>
    .menus{
        width: 190px;
        height: 480px;
        background: #6e6568;
        margin-right: 10px;
        color:#fff;
        font-size: 14px;
        position: relative;
        left:0;
        top:0;
    }
    .cate_menu{
        padding-left:12px;
        width: 190px;
        height: 38px;
        cursor: pointer;
    }
    .cate_menu span:hover{
        color: red;

    }
    .fcate_menu{
        margin-top: 10px;
    }
    .loyou{
        width: 810px;
        height: 480px;
        position: absolute;
        left:190px;
        top:0;
        /*background: red;*/
        color: #000;
        text-align: center;
        line-height: 380px;
        font-size: 20px;
        border: 1px solid #ccc;
        background: #fff;
        z-index: 99999999999;
        margin-top: -1px;
    }
    .l_a,.l_b,.l_c,.l_d,.l_e,.l_f,.l_g,.l_h,.l_i,.l_j,.l_k,.l_l{
        display: none;
    }
    .cate_a:hover .l_a{
        display: block;
    }
    .cate_b:hover .l_b{
        display: block;
    }
    .cate_c:hover .l_c{
        display: block;
    }
    .cate_d:hover .l_d{
        display: block;
    }
    .cate_e:hover .l_e{
        display: block;
    }
    .cate_f:hover .l_f{
        display: block;
    }
    .cate_g:hover .l_g{
          display: block;
      }
    .cate_h:hover .l_h{
        display: block;
    }
    .cate_i:hover .l_i{
        display: block;
    }
    .cate_j:hover .l_j{
          display: block;
      }
    .cate_k:hover .l_k{
            display: block;
        }
    .cate_l:hover .l_l{
        display: block;
    }
</style>