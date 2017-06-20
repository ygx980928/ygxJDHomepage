<template>
  <div id="dbx">
      <div class="navbg"></div>
      <div class="bx">
          <nav-a></nav-a>
          <search></search>
      </div>

  </div>
</template>
<script>
    import     navA   from './nav.vue'
    import   search    from  './search.vue'
    export default{
        data(){
            return{
            }
        },
        components:{
              navA,
            search
        }
    }
</script>
<style>
    #dbx{
        width: 100%;
        font-size: 12px;
        color:#989898;
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