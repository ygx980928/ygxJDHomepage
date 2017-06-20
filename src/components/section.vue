<template>
  <div id="boxa">
      <!--中间部分start-->
     <div class="bg_b">
         <menua class="fl"></menua>
         <lft class="fl"></lft>
         <col3 class="fl"></col3>
     </div>
     <!--end-->
  </div>
</template>
<script>
    import menua from './middle/menu.vue'
    import lft   from './middle/lft.vue'
    import col3  from './middle/col3.vue'
    export default {
        name: 'boxa',
        data () {
            return {
            }
        },
        components:{
            menua,
            lft,
            col3
        }
    }
</script>
<style >
    #boxa{
        width: 100%;
        height: 480px;
        z-index: 9846386;
        background:url("../images/594y.png")no-repeat 50% 0 ;
    }
    .bg_b {
        width: 1190px;
        height: 480px;
        margin: 0 auto;
    }
</style>