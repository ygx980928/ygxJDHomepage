<template>
  <div id="app">
    <advertising></advertising>
    <!--头部广告-->
   <typerarea></typerarea>
    <!--版心-->
  </div>
</template>
<script>
  import advertising from './components/advertising.vue'
  import typerarea from './components/Typearea.vue'
  export default {
  name: 'app',
  data () {
    return {
    }
  },
    components:{
      advertising,
      typerarea
    }
}
</script>


