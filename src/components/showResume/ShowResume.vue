<template>
    <div id="show-resume">
        <div v-html="resStyleCode"></div>
       <div class="d1">
           <h2>xxx1</h2>
           <p>{{resumeData.d1.name}}</p>
           <h2>xx2</h2>
           <p>{{resumeData.d1.age}}</p>
           <h2>xx3</h2>
           <p>{{resumeData.d2.experience}}</p>
       </div>
    </div>
</template>

<script type="text/ecmascript-6">
    export default{
        data(){
            return{
                msg:'hello vue',
                resStyleCode:"",
                resumeData:{
                    d1:{
                        name:'zhangxx',
                        age:233
                    },
                    d2:{
                       'experience':'华盛顿圣诞节大家都会客户收到货看电视说的很对短开始结合实际客户端收到货华盛顿看看'
                    }
                }
            }
        },
        methods:{
            responseStyleCode: function (code) {
                this.resStyleCode = "<style>"+code+"</style>"
            }
        },
        components:{
           
        }
    }
</script>

<style>

    #show-resume{
        float: left;
        width: 50%;
        height: 100%;
        background: #ed85b6;
    }
    /*h2{*/
        /*color: aliceblue;*/
        /*text-align: center;*/
    /*}*/
    /*p{*/
        /*color: #328c63;*/
        /*text-align: center;*/
        /*border: 1px solid rebeccapurple;*/
        /*width: 80%;*/
        /*margin: 0 auto;*/
    /*}*/
</style>