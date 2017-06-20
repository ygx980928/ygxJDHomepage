<template>
    <div class="col3" id="col3">
        <div class="user">
            <img src="../../images/user.jpg">
            <p v-text="jd"></p>
            <b><a href="#">登录</a> <a href="#">注册</a></b>
            <div class="couple">新人福利</div>
            <div class="couple-a">PLUS&nbsp;会员</div>
        </div>
        <div class="news">
            <div class="news_a clearfix">
                <a href="#" class="fl">促销</a>
                 <span style="color: #ccc" class="fl">|</span>
                <a href="#" class="fl ">公告</a>
                <a href="#" class="fr">更多</a>
            </div>
            <p><a href="#">最后一天 跨万店3免1</a> </p>
            <p><a href="#">京东超市满 199减100！</a> </p>
            <p><a href="#">抢618减300神券，最后一天</a> </p>
            <p><a href="#">每日享折扣 京东品质游</a> </p>
            <p><a href="#">沃尔玛与京东合作再升级 </a> </p>
        </div>

        <div class="j-s">
            <p>
                <span style="border-top: 2px solid red">话费 </span>
                <span>机票</span>
                <span>酒店</span>
                <span>游戏</span>
            </p>
            <div class="huafei" style="font-size: 12px;margin-top: 10px">
                <span>话费充值</span>
                <span>流量充值</span>
                <span>套餐充值</span>
            </div>
            <p style="margin-top: 20px;font-size: 13px">
                <span>号码</span>
                <span>
                    <input type="text" placeholder="请输入号码" style="width: 93px;height: 20px; "/>
                </span>
            </p>
            <p style="margin-top: 20px;font-size: 13px">
                <span>面值</span>
                <span>
                   <select>
                       <option>100元</option>
                       <option>200元</option>
                       <option>300元</option>
                   </select>
                </span>
            </p>
           <input type="submit" class="jd-av" value="快速充值"/>
            <div class="bot"> <span style="font-size: 10px" >hot</span> <a href="#">抢50元话费充值券</a> </div>
        </div>
    </div>
</template>
<script>
    export default{
        name:'col3',
        data(){
            return{
                jd:'HI!欢迎来到京东！'
            }
        }
    }
</script>
<style>
    .col3{
        width: 190px;
        height: 480px;
        position: relative;
    }
    .user{
        width: 190px;
        height:116px;
        color: #666;
        border-bottom: 1px solid #e6e6e6;
        position: relative;
    }
    .user img{
        position: absolute;
        left: 20px;
        top:10px;
    }
    .user p{
        font-size: 12px;
        width: 100px;
        height: 18px;
        font-size: 12px;
        position: absolute;
        right: 2px;
        top:20px;
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;
    }
    .user b{
        position: absolute;
        right: 42px;
        top:35px;
    }
    .user b a{
          color: #666;
          font-size: 12px;
      }
    .user b a:hover{
        color: red;
    }
    .couple{
        display: inline-block;
        margin-right: 10px;
        width: 70px;
        height: 20px;
        border: 2px solid #e01222;
        line-height: 20px;
        font-size: 12px;
        text-align: center;
        color: #e01222;
        position: absolute;
        left:20px;
        bottom: 15px;
        cursor: pointer;
    }
    .couple-a{
        display: inline-block;
        margin-right: 10px;
        width: 70px;
        height: 20px;
        border: 2px solid #e01222;
        line-height: 20px;
        font-size: 12px;
        text-align: center;
        color: #e01222;
        position: absolute;
        bottom: 15px;
        left:100px;
        cursor: pointer;
    }
    .news{
        width: 190px;
        height: 145px;
        /*background: red;*/
    }
    .news_a{
        width: 100%;
        height:27px;
        border-bottom: 1px solid #ccc;
    }
    .news_a a{
        color: #333;
        margin-right: 10px;
        margin-left: 10px;
        font-size: 13px;
        text-align: center;
        line-height:27px;
    }
    .news_a a:hover{
        color: red;
    }
    .news p a:hover{
        color: red;
    }
    .news p a{
        border-top: 2px solid #fff;
        color: #666;
        font-size: 12px;
        text-indent: 2em;
        margin-left: 10px;
    }
    .j-s{
        width: 190px;
        height: 210px;
        border-top: 1px solid #ccc;
        color:#666;
        font-size: 15px;
        border-right: 1px solid #ccc;
        border-left: 1px solid #ccc;
        border-bottom: 1px solid #ccc;
    }
    .j-s>p>span{
        border-left:1px solid #ccc;
        width: 40px;
        text-align: center;
        display: inline-block;
    }
    .jd-av{
        width: 85px;
        height: 25px;
        color: #fff;
        background: red;
        font-size: 12px;
        border: none;
        text-align: center;
        margin-top: 10px;
        margin-left: 30px;
    }
    .huafei span{
        width: 20px;
        margin-left: 8px;
    }
    .huafei span:hover{
        background: red;
        color: #fff;
        cursor: pointer;
    }
    .bot{
       width: 100%;
        height: 14px;
        margin-left: 20px;
        margin-top: 10px;
    }
    .bot span{
        display: inline-block;
        width: 34px;
        height: 14px;
        background: blue;
        color: #fff;
        border-radius: 3px;
        text-align: center;
        line-height:14px;
    }
    .bot a{
        color: blue;
        font-size: 10px;
    }
</style>