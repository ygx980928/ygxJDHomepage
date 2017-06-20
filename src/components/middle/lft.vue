<template>
<div class="lft" id="lft">
    <div class="demo">
        <ul class="point">
            <li v-for="(curpoint,index) in point"  :class="{hovers:curIndex==index?flag:''}">{{curpoint}}</li>
        </ul>
        <transition-group name="flip-list" tag="ul">
            <li v-for="curImg in currImgs" v-bind:key="curImg" class="list-item">
                <img :src="curImg">
            </li>
        </transition-group>
         <div class="loe"></div>

    </div>
    <div class="lt">
        <img src="../../images/2222.jpg" width="390" height="130">
        <img src="../../images/66.jpg" width="390" height="130" style="margin-left: 5px">
    </div>
</div>
</template>
<script>
    export default{
        name:'lft',
        data(){
           return{
               point:['','','',''],
               currImgs: [],
               curpoint:[],
               curIndex:0,
               flag:true,
               imgs: [
                   'https://img11.360buyimg.com/da/jfs/t4000/107/2234194410/85271/6c24d985/58a50cafNb60886c9.jpg',
                   'https://img20.360buyimg.com/da/jfs/t3154/175/5917485830/129679/f123634c/5897e6a2N83837dd2.jpg',
                   'https://img1.360buyimg.com/da/jfs/t3133/89/5984232745/66970/beaf615c/589ac9bcNe544a72e.jpg',
                   'https://img20.360buyimg.com/da/jfs/t3157/165/6117849901/102894/88bf53b8/589d67b6Ne8986a9e.jpg'
               ],
               index: 0
           }
        },
        mounted: function () {
            this.currImgs = [this.imgs[0]];
            this.startChange();
            this.curpoint=[this.point[0]]
        },
        methods: {
            startChange: function () {
                var _this = this;
                setInterval(function () {
                    if (_this.index < _this.imgs.length - 1) {
                        _this.index++
                    } else {
                        _this.index = 0
                    }
                    _this.currImgs.splice(0, 1, _this.imgs[_this.index]);
                    _this.curIndex = _this.index
                }, 3000);
            }
        }

    }
</script>
<style>
    .point{
        width: 150px;
        height: 20px;
        background-color: hsla(0,0%,100%,.3);
        position: absolute;
        bottom: 150px;
        left: 50%;
        margin-left: -75px;
        z-index: 100;
        border-radius: 12px;
    }
    .point li{
           width: 12px;
           height: 12px;
          background: #fff;
          margin-left: 14%;
          margin-top: 5px;
           float: left;
        border-radius: 50%;
    }
    .loe{
        width: 75px;
        height: 100px;
        background: url("../../images/61866.png");
        position: absolute;
        left:30px;
        top:0;
    }
    .lft{
        width: 790px;
        height: 100%;
        /*background: #f90;*/
        margin-right: 10px;
        position: relative;
    }
    .demo{
        width: 790px;
        height: 340px;
        /*background: red;*/
        cursor: pointer;
    }
    .lt{
        width: 100%;
        height: 130px;
        /*background: blue;*/
        margin-top: 10px;
    }
    img { border: 0 none; }
    input, select { vertical-align: middle; }
    table { border-collapse: collapse; }
    s, em, i { font-style: normal; text-decoration: none; }
    a { outline: none; text-decoration: none; }
    a:hover { text-decoration: underline; }
    .clear { *zoom: 1; }
    .clear:after { clear: both; content: "."; display: block; height: 0; overflow: hidden; visibility: hidden; zoom: 1; }
    .flip-list-enter-active, .flip-list-leave-active {
        transition: all 1s;
    }
    .flip-list-enter, .flip-list-leave-active {
        opacity: 0;
    }
    .list-item{
        position: absolute;
        top: 0;
        left: 0;
    }
    .point .hovers{
        background: red;
    }
</style>
