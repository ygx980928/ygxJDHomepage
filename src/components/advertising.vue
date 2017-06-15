<template>
    <transition name="fade">
    <div class="advertising" v-bind:title="msg" v-if="box_1">

        <a href="#">
            <div class="soe"></div>
            <i id="advsd" v-bind:title="advsd" v-on:click="showhide">×</i>
        </a>
    </div>
    </transition>
</template>
<script>
 export default{
     data(){
         return{
             msg: 'This is advertising',
             advsd:'关闭',
             box_1:true,
         }
     },
     methods:{
         showhide(){
             this.box_1=false
         }
     }
 }
</script>
<style>
    .advertising {
        width: 100%;
        height: 80px;
        background-color: red;
        display: block;
        position: relative;
        left: 0;
        top: 0; }
    .fade-enter-active, .fade-leave-active {
        transition: opacity .5s
    }
    .fade-enter, .fade-leave-active {
        opacity: 0
    }
    .advertising a {
        width: 1190px;
        height: 80px;
        background: url("../images/advertising.jpg");
        position: absolute;
        left: 50%;
        margin-left: -595px; }
    .advertising a i {
        width: 20px;
        height: 20px;
        background: #2d2d2d;
        opacity: 0.4;
        filter: alpha(opacity=40);
        color: #fff;
        position: absolute;
        right: 3px;
        top: 3px;
        cursor: pointer;
        font-style: normal;
        font-size: 25px;
        line-height: 20px;
        text-align: center;
        z-index: 999;
        transition: all 1s ease;
    }
    .soe {
        width: 150px;
        height: 80px;
        background: url("../images/618.jpg");
        position: absolute; }

</style>