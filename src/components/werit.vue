<template>
    <div id="wer">

    </div>
</template>
<script>
    export default{
        name:'wer',
        data(){
            return{

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
    #wer{
        width: 100px;
        height:100px;
    }
</style>