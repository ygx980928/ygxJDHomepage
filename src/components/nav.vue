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
                address:['北京','上海','天津','重庆','河北','山西','河南','辽宁','吉林','黑龙江','内蒙古','江苏','山东','安徽','浙江','福建','湖北','湖南','广东','广西','江西','四川','海南','贵州','云南','西藏','陕西','甘肃','青海','宁夏','新疆','港澳','台湾','钓鱼岛','海外']
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
    *{
        font-size: 12px;
        color:#989898;
    }
    nav{
        width: 1190px;
        height: 30px;
        background: #ddd;
        z-index: 2231;
        border:none;
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
        /*border: 1px solid #000;*/
        display:none;

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
</style>