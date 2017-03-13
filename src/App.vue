<template>
    <div id="app">
        <ShowMenu></ShowMenu>
        <ShowStyle ref="comShowStyle"></ShowStyle>
        <ShowResume ref="comShowResume"></ShowResume>
    </div>
</template>

<script>
    import Hello from './components/Hello'
    import ShowMenu from './components/menu/ShowMenu.vue'
    import ShowStyle from './components/showStyle/ShowStyle.vue'
    import ShowResume from './components/showResume/ShowResume.vue'

    export default {
        name: 'app',
        data(){
            return{
                code:`
                h2{
                color: aliceblue;
                text-align: center;
                }
                p{
                    color: #328c63;
                    text-align: center;
                    border: 1px solid rebeccapurple;
                    width: 80%;
                    margin: 0 auto;
                }
                `
            }
        },
        created(){
            let n = 0;
            let _this = this;

//            this.$nextTick(function () {
//                setInterval(function () {
//                    _this.$refs.comShowStyle.writeStyleCode(_this.code.substring(0,n));
//                    _this.$refs.comShowResume.responseStyleCode(_this.code.substring(0,n));
//                    n++;
//                },100);
//             })
         },
        methods:{
            setStyleCode:function(){
                this.$refs.comShowStyle.writeStyleCode('ss');
            }
        },
        components: {
            Hello,
            ShowMenu,
            ShowStyle,
            ShowResume
        }
    }
</script>

<style >

    /* 内外边距通常让各个浏览器样式的表现位置不同 */
    body, div, dl, dt, dd, ul, ol, li, h1, h2, h3, h4, h5, h6, pre, code, form, fieldset, legend, input, textarea, p, blockquote, th, td, hr, button, article, aside, details, figcaption, figure, footer, header, hgroup, menu, nav, section {
        margin: 0;
        padding: 0;
    }

    input, select, textarea {
        font-size: 100%;
    }
    input{outline: none;}

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
    /*清除浮动代码*/
    .clearfloat:after{display:block;clear:both;content:"";visibility:hidden;height:0}
    .clearfloat{zoom:1}
    body, html {
        width: 100%;
        height: 100%;
        padding: 0;
        margin: 0;
        min-width: 950px;
        font-size: 62.5%;
    }

    #app {
        width: 100%;
        height: 100%;
    }
</style>
