<template>
    <div id="app">
    <advertising></advertising>
    <!--头部广告-->
    <typerarea></typerarea>
    <!--版心-->
    <tbar></tbar>
    <!--right guanggao-->
    <sectiona></sectiona>
    <werit></werit>
    <jdbar></jdbar>
    </div>
</template>
<script>
  import advertising from './components/advertising.vue'
  import typerarea   from './components/Typearea.vue'
  import tbar        from './components/tbar.vue'
  import sectiona    from  './components/section.vue'
  import werit       from  './components/werit.vue'
  import jdbar       from  './components/jd_bar.vue'
  export default {
  name: 'app',
  data () {
    return {
    }
  },
    components:{
      advertising,
      typerarea,
       tbar,
        sectiona,
        werit,
        jdbar
    }
}
</script>
<style>
    html,body{
        /*overflow: hidden;*/
    }

    .jia{
        width: 100000px;
        height: 1000px;
        background: red;
    }
</style>


