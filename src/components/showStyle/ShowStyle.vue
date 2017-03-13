<template>
    <div id="show-style">
       <pre class="style-code" v-html="styleMsg"></pre>
    </div>
</template>

<script type="text/ecmascript-6">
    export default{
        data(){
            return{
                msg:'hello vue',
                styleMsg:''
            }
        },
        created(){

        },
        methods:{
            writeStyleCode: function (code) {
                this.styleMsg = code;
            }
        },
        watch(){

        },
        components:{
           
        }
    }
</script>

<style>
    #show-style{
        position: relative;
        float: left;
        width: 40%;
        height: 100%;
        background: #ffffff;
    }
    .style-code{
        position: absolute;
        top:0;
        left: 0;
        right: 0;
        bottom: 0;
        width: 80%;
        height: 90%;
        border: 1px solid rebeccapurple;
        margin: auto auto;
        padding: 20px;
    }
</style>