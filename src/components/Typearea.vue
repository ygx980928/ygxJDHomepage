<template>
  <div id="dbx">
      <div class="navbg"></div>
      <div class="bx">
          <nav-a></nav-a>
      </div>

  </div>
</template>
<script>
    import     navA   from './nav.vue'
    export default{
        name:'bx',
        data(){
            return{

            }
        },
        components:{
              navA
        }
    }
</script>
<style>
    #dbx{
        width: 100%;
    }
    .bx{
        width: 1190px;
        margin: 0 auto;
    }
    .navbg{
        width: 100%;
        height: 30px;
        background: #ddd;
        position: absolute;
        z-index: -1;
    }
</style>