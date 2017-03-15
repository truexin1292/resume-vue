<template>
    <div id="app">
        <ShowMenu v-on:listenShowMenu='listenShowMenu'></ShowMenu>
        <ShowStyle ref="comShowStyle"></ShowStyle>
        <ShowResume ref="comShowResume" :resumeData="resumeData"></ShowResume>
        <transition name="fade">
            <FormList ref="comFormList" :resumeData="resumeData" v-if="formListShow" v-on:listenFormList='listenFormList'></FormList>
        </transition>
     </div>
</template>

<script>
    import Hello from './components/Hello'
    import ShowMenu from './components/menu/ShowMenu.vue'
    import ShowStyle from './components/showStyle/ShowStyle.vue'
    import ShowResume from './components/showResume/ShowResume.vue'
    import FormList from './components/form/FormList.vue'
    import resumeData from '../static/resumedata.json'

    export default {
        name: 'app',
        data(){
            return{
                fromDataT:{},
                formListFlag:false,
                formListShow:false,
                resumeData:resumeData,
                code:` .section-left i{
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
.edu .honor-title{
    font-size: 1.8rem;
    color: #3d3d3d;
    font-weight: 500;
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
.skill h3{
    margin-bottom: 1rem;
}
.skill .sk{
    position: relative;
    width: 90%;
    margin: 0 auto;
    text-align: left;
    text-indent: 1.5rem;
    font-size: 1.6rem;
}
.skill .sk-wrap{
    position: absolute;
    top:0;
    right: 0;
    bottom: 0;
    margin: auto 0;
    width: 70%;
    height: 1rem;
    border-radius: 0.5rem;
    background:  rgba(151, 151, 151,0.5);
}
.skill .sk-per{
    display: block;
    width: 90%;
    height: 100%;
    background: rgba(151, 151, 151,0.9);
    border-radius: 0.4rem;
}

/* section-right  blog
 ------------------------------------*/
.section-right .blog-box{
    margin-bottom: 1rem;
    /*background: linear-gradient(to right, #ffffff, rgba(135, 135, 135, 0.5));*/
    /*box-shadow: 4px 4px 8px 0 rgba(0,0,0,0.2);*/

}
.section-right .blog{
    float: right;
    font-size: 1.4rem;
    margin-right: 2rem;
}
.blog .title-name{
    font-size: 1.6rem;
}
.blog .title-name:after{
    content: '';
    height: 2px;
    width: 100%;
    display:block;
    margin-bottom: 2px;
    /*background: linear-gradient(to right, #ffffff, rgba(135, 135, 135, 0.5) 50%, #ffffff);*/
}
.blog .link{
    line-height: 2rem;
    margin-bottom: 2px;
    padding-right: 0.5rem;
    /*background: linear-gradient(to right, #ffffff, rgba(135, 135, 135, 0.5));*/

}
.blog .link:nth-child(2n+1){
    /*background: linear-gradient(to right, #ffffff, rgba(135, 135, 135, 0.5));*/
}
.blog .link i{
    margin-right: 1rem;
}
.blog .link a{
    color: #313131;
}
/* section-right  experience
 ------------------------------------*/
.experience{
    padding: 0.5rem;
    box-sizing: border-box;
    font-size: 1.4rem;
    margin-bottom: 1rem;
    /*box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);*/
}
/*.experience:hover {*/
/*box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);*/
/*}*/
.experience .title{
    width: 100%;
    height: 2rem;
}
.experience .title:after{
    content: '';
    height: 2px;
    width: 100%;
    display:block;
    margin-bottom: 2px;
    background: linear-gradient(to right, #ffffff, rgba(135, 135, 135, 0.5) 50%, #ffffff);
}
.title .title-name{
    font-size: 1.8rem;
    display: inline-block;
}
.title .title-date{
    float: right;
}
.experience .item-title{
    padding: 0.6rem 0;
    color: #42b983;
}
.experience .item-title span{
    display: inline-block;
}
.item-title .item-name{
    font-size: 1.6rem;
}
.item-title .item-skill{

}
.item-title .item-date{
    float: right;
}
.experience .item ul{
    margin-left: 1.5rem;
    list-style: circle;
}
.self-evaluation .title{
    margin-bottom: 1rem;
}
.self-evaluation p{
    line-height: 1.4;
}`
            }
        },
        created(){
            let n = 0;
            let _this = this;

            this.$nextTick(function () {
                setInterval(function () {
                    _this.$refs.comShowStyle.writeStyleCode(_this.code.substring(0,n));
                    _this.$refs.comShowResume.responseStyleCode(_this.code.substring(0,n));
                    n++;
                },10);
             })
         },
        methods:{
            setStyleCode:function(){
                this.$refs.comShowStyle.writeStyleCode('ss');
            },
            downloadPdf:function(){
                var htmlcode = document.getElementById('show-resume');
                html2canvas(htmlcode, {
                    onrendered: function(canvas) {
                        document.body.appendChild(canvas);
                    },
//                    width: 1487,
//                    height: 2105
                });
            },
            listenShowMenu: function (msg) {
                if(msg.type == 'fileClick'){
                    this.formListShow = msg.showFlag;
                    if(this.formListFlag){
                        this.resumeData.formFlag = true;
                    }
                }
                if(msg.type == 'kaClick'){
                    var htmlcode = document.getElementById('show-resume');
                    html2canvas(htmlcode, {
                        onrendered: function(canvas) {
                            document.body.appendChild(canvas);
                        },
                    //width: 1487,
                    //height: 2105
                    });
                }
             },
            listenFormList: function (msg) {
                if(msg.type == "createResClick"){
                    this.formListShow = msg.showFlag;
                }
                if(msg.type == "fromData"){
                    this.resumeData = msg.fromData;
                    this.formListFlag = true;
                }
            }
        },
        components: {
            Hello,
            ShowMenu,
            ShowStyle,
            ShowResume,
            FormList
        }
    }
</script>

<style >

    /* 内外边距通常让各个浏览器样式的表现位置不同 */
    body, div, dl, dt, dd, ul, ol, li, h1, h2, h3, h4, h5,
    h6, pre, code, form, fieldset, legend, input, textarea,
    p, blockquote, th, td, hr, button, article, aside, details,
    figcaption, figure, footer, header, menu, nav, section {
        margin: 0;
        padding: 0;
    }

    input, select, textarea {
        font-size: 100%;
    }
    input{outline: none;
        border-style:none}

    /* 去掉各 Table  cell 的边距并让其边重合 */
    table {
        border-collapse: collapse;
        border-spacing: 0;
    }

    /* 去除默认边框 */
    fieldset, img {
        border: 0;
    }

    /* 去掉 firefox 下此元素的边框 */
    abbr, acronym {
        border: 0;
        font-variant: normal;
    }

    /* 一致的 del 样式 */
    del {
        text-decoration: line-through;
    }

    address, caption, cite, code, dfn, em, th, var {
        font-style: normal;
        font-weight: 500;
    }

    /* 去掉列表前的标识, li 会继承 */
    ol, ul {
        list-style: none;
    }

    /* 对齐是排版最重要的因素, 别让什么都居中 */
    caption, th {
        text-align: left;
    }
    a{
        text-decoration:none;
    }
    /*清除浮动代码*/
    .clearfloat:after{display:block;clear:both;content:"";visibility:hidden;height:0}
    .clearfloat{zoom:1}
    body, html {
        width: 100%;
        height: 100%;
        padding: 0;
        margin: 0;
        min-width: 1024px;
        font-size: 62.5%;
    }

    #app {
        width: 100%;
        height: 100%;
    }
    .fade-enter-active, .fade-leave-active {
        transition: opacity .5s
    }
    .fade-enter, .fade-leave-active {
        opacity: 0
    }
</style>
