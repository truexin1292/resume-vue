<template>
    <div id="show-resume">
        <section class="section-left">
            <div class="head">
                <h2>曾田生</h2>
                <h3>求职岗位:前端开发</h3>
                <p><i class="icon-phone icon-2x"></i></p>
                <p>12345678901</p>
                <p><i class="icon-envelope-alt icon-2x"></i></p>
                <p>zengtianshengz@163.com</p>
                <ul class="clearfloat">
                    <li>
                        <p>住址</p>
                        <p>杭州余杭</p>
                    </li>
                    <li>
                        <p>年龄</p>
                        <p>1992.9.25</p>
                    </li>
                    <li>
                        <p>性别</p>
                        <p>男</p>
                    </li>
                </ul>
            </div>
            <div class="edu">
                <h3><span class="item-title">教育背景</span></h3>
                <p><span>华侨大学厦门工学院</span><span>本科</span></p>
                <p>2012-9-1 至 2016-7-1</p>
                <p>专业:电子信息工程及自动化</p>
                <p>荣获</p>
                <p>2014年省电子科技大赛3等奖</p>
            </div>
            <div class="interest">
                <h3><span class="item-title">兴趣爱好</span></h3>
                <p><span class="inte-span">骑行</span><span class="inte-span">篮球</span></p>
                <p><span class="inte-span">编程</span><span class="inte-span">音乐</span></p>
            </div>
            <div class="skill">
                <h3><span class="item-title">技能特长</span></h3>
                <div class="sk">
                    <div class="cg-wrap cg-js">
                        <div class="cg-in-wrap cg-in-js"></div>
                        <div class="cg-in">js</div>
                    </div>
                    <div class="cg-wrap cg-css">
                        <div class="cg-in-wrap cg-in-css"></div>
                        <div class="cg-in">css</div>
                    </div>
                    <div class="cg-wrap cg-html">
                        <div class="cg-in-wrap cg-in-html"></div>
                        <div class="cg-in">html</div>
                    </div>
                </div>

            </div>
        </section>
        <section class="section-right">
            <div class="blog">
                <div class="github"><span class="icon-green">github:</span>https://github.com/ZengTianShengZ</div>
                <div class="personal-blog"><span class="icon-green">blog1:</span>https://github.com/ZengTianShengZ</div>
                <div class="personal-blog2"><span class="icon-green">blog2:</span>https://github.com/ZengTianShengZ</div>
            </div>
            <div class="work-experience">
                <div class="title">
                    <div class="title-name">gongzuojingyan</div>
                    <div class="title-date">200-1-2-2-zhijaing</div>
                </div>
                <div class="item">
                    <div class="item-title">
                        <div class="item-name">xxxx</div>
                        <div class="item-date">22-22-22-22</div>
                    </div>
                    <div class="item-detail">dkdkk</div>
                 </div>
            </div>
            <div class="project-experience">
                <div class="title">
                    <div class="title-name">gongzuojingyan</div>
                    <div class="title-date">200-1-2-2-zhijaing</div>
                </div>
                <div class="item">
                    <div class="item-title">
                        <div class="item-name">xxxx</div>
                        <div class="item-date">22-22-22-22</div>
                    </div>
                    <div class="item-detail">dkdkk</div>
                </div>
            </div>
            <div class="skill-experience">
                <div class="title">
                    <div class="title-name">gongzuojingyan</div>
                    <div class="title-date">200-1-2-2-zhijaing</div>
                </div>
                <div class="item">
                    <div class="item-title"></div>
                    <div class="item-detail">dkdkk</div>
                </div>
            </div>
            <div class="self-evaluation">
                <div class="title">
                    <div class="title-name">gongzuojingyan</div>
                    <div class="title-date">200-1-2-2-zhijaing</div>
                </div>
                <p class="eval-detail"></p>
            </div>
        </section>


        <div v-html="resStyleCode"></div>
    </div>
</template>

<script type="text/ecmascript-6">
    export default{
        data(){
            return{
                msg:'hello vue',
                resStyleCode:"",
                resumeData:{

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
        background: #ffffff;
    }
    /* section-left
    ------------------------------------*/
    .section-left{
        float: left;
        width: 30%;
        height: 100%;
        text-align: center;
        color: #313131;
        background: rgb(249,249,249);
        line-height: 1.8;
    }
    .section-left i{
        color: rgb(151, 151, 151);
        font-size: 1.5rem;

    }
    .section-left h2{
        font-size: 2.5rem;
    }
    .section-left h3{
         font-size: 2rem;
    }
    .section-left p{
        font-size: 1.5rem;
    }
    /* head
    ------------------------------------*/
    .section-left .head{
        padding-top: 2rem;
        background: rgb(236,236,236);

    }
    .head ul{
        width: 100%;
        margin: 1rem 0;
        border-top: 2px solid rgba(151, 151, 151,0.5);
        border-bottom:2px solid rgba(151, 151, 151,0.5);
    }
    .head ul li{
        float: left;
        width: 32.1%;
    }
    .head ul li + li{
        border-left: 2px solid rgba(151, 151, 151,0.5);
    }
    .section-left .item-title{
        border-bottom: 2px solid rgba(151, 151, 151,0.5);
        padding: 0 0.4rem;
    }
    /* edu
    ------------------------------------*/
    .section-left .edu{
        line-height: 2;
        margin-bottom: 0.8rem;
    }
    /* interest
    ------------------------------------*/
    .section-left .interest{
        margin-bottom: 0.8rem;

    }
    .section-left .inte-span{
        display: inline-block;
        font-size: 1.4rem;
        border: 1px solid rgba(151, 151, 151,0.5);
        padding: 0 1rem;
        margin: 0.2rem 1rem;
        border-radius: 1rem;
    }
    /* skill
    ------------------------------------*/
    .section-left .skill{
        width: 100%;
    }
    .skill .sk{
        width: 100%;
        position: relative;
        margin: 0.8rem 0;
    }
    .skill .cg-wrap{
        position: absolute;
        top:0;
        left:0;
        width: 30%;
        height: 0;
        padding-bottom: 30%;
        background: rgba(135, 135, 135, 0.5);
        border-radius: 50%;
    }
    .cg-wrap .cg-in-wrap{
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        border-radius: 50%;
        background: rgba(58, 58, 58, 0.5);
    }
    .cg-wrap .cg-in{
        position: absolute;
        top:0;
        left: 0;
        right: 0;
        bottom: 0;
        width: 85%;
        height: 85%;
        margin: auto auto;
        background: #ffffff;
        border-radius: 50%;
        font-size: 1.6rem;
        line-height: 4rem;
    }
    .sk .cg-js{
        left:0;
    }
    .sk .cg-css{
        left: 34%;
    }
    .sk .cg-html{
        left: 68%;
    }
    .sk .cg-in-js{
        clip: rect(30px, auto, auto, 0px);
    }
    .sk .cg-in-css{
        clip: rect(20px, auto, auto, 0px);
    }
    .sk .cg-in-html{
        clip: rect(10px, auto, auto, 0px);
    }






    .section-right{
        float: left;
        width: 69%;
        height: 100%;
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