<template>
    <div id="from_box">
        <div class="from-content">
            <div class="from-content-item">
                <div class="item">
                    <div class="item-head">个人基本资料</div>
                    <div class="item-content clearfloat">
                        <div class="inp-short">姓名:<input type="text"></div>
                        <div class="inp-short">意向:<input type="text"></div>
                        <div class="inp-short">性别:<input type="text"></div>
                        <div class="inp-short">年龄:<input type="text" placeholder="1770.8.23"></div>
                        <div class="inp-short">毕业学校:<input type="text"></div>
                        <div class="inp-short">学历:<input type="text"></div>
                        <div class="inp-short">毕业时间:<input type="text" placeholder="2012-9 至 2016-7"></div>
                        <div class="inp-short">荣获:<input type="text" placeholder="多份殊荣逗号隔开"></div>
                        <div class="inp-short">兴趣爱好:<input type="text" placeholder="逗号隔开"></div>
                        <div class="inp-short">技能特长:<input type="text" placeholder="最多三个特长逗号隔开"></div>
                    </div>
                    <div class="item-footer"><i></i>&nbsp;&nbsp;&nbsp;</div>
                </div>

                <div class="item">
                    <div class="item-head">技术链接</div>
                    <div class="item-content">
                        <div class="inp-long">GitHub:<input type="text" placeholder="选填"></div>
                        <div class="inp-long">技术博文:<input type="text" placeholder="选填"></div>
                        <div class="inp-long">个人博客:<input type="text" placeholder="选填"></div>
                    </div>
                    <div class="item-footer"><i></i>&nbsp;&nbsp;&nbsp;</div>
                </div>

                <div class="item">
                    <div class="item-head">
                        <span>工作经验</span>
                        <span class="item-head-time">时间:<input type="text" placeholder="2001-2 至 今"></span>
                    </div>
                    <div class="item-content">
                        <div class="contt clearfloat">
                            <div class="inp-short">项目名称:<input type="text" placeholder=""></div>
                            <div class="inp-short">项目技术:<input type="text" placeholder=""></div>
                            <div class="inp-short">项目时间:<input type="text" placeholder="2001-2 至 今"></div>
                        </div>
                        <div class="inp-long inp-long-more">项目简介:
                            <input type="text" placeholder="1、">
                            <input type="text" placeholder="2、">
                            <input type="text" placeholder="3、">
                        </div>
                    </div>
                    <div class="item-footer"><i class=" icon-plus-sign-alt icon-1x"></i>&nbsp;&nbsp;&nbsp;</div>
                </div>

                <div class="item">
                    <div class="item-head">
                        <span>项目经验</span>
                        <span class="item-head-time">时间:<input type="text" placeholder="2001-2 至 今"></span>
                    </div>
                    <div class="item-content">
                        <div class="contt clearfloat">
                            <div class="inp-short">项目名称:<input type="text" placeholder=""></div>
                            <div class="inp-short">项目技术:<input type="text" placeholder=""></div>
                            <div class="inp-short">项目时间:<input type="text" placeholder="2001-2 至 今"></div>
                        </div>
                        <div class="inp-long inp-long-more">项目简介:
                            <input type="text" placeholder="1、">
                            <input type="text" placeholder="2、">
                            <input type="text" placeholder="3、">
                        </div>
                    </div>
                    <div class="item-footer"><i class=" icon-plus-sign-alt icon-1x"></i>&nbsp;&nbsp;&nbsp;</div>
                </div>

                <div class="item">
                    <div class="item-head">掌握技能</div>
                    <div class="item-content">
                        <div class="contt clearfloat">
                            <div class="inp-short">技能分类:<input type="text" placeholder=""></div>
                        </div>
                        <div class="inp-long inp-long-more">简介:
                            <input type="text" placeholder="1、">
                            <input type="text" placeholder="2、">
                            <input type="text" placeholder="3、">
                        </div>
                    </div>
                    <div class="item-footer"><i class=" icon-plus-sign-alt icon-1x"></i>&nbsp;&nbsp;&nbsp;</div>
                </div>

                <div class="item last-item">
                    <div class="item-head">自我评价</div>
                    <div class="item-content">
                        <div class="inp-long inp-long-more">评价:
                            <input type="text" placeholder="1、">
                            <input type="text" placeholder="2、">
                            <input type="text" placeholder="3、">
                        </div>
                    </div>
                    <div class="item-footer"><i class=" icon-plus-sign-alt icon-1x"></i>&nbsp;&nbsp;&nbsp;</div>
                </div>
            </div>
            <div class="xs"></div>
            <div class="xs2"></div>
            <div class="from-box-footer">
                <div class="butt">生成</div>
            </div>
        </div>
     </div>
</template>

<script type="text/ecmascript-6">
    export default{
        data(){
            return {
                msg: 'hello vue'
            }
        },
        components: {}
    }
</script>

<style>
    #from_box {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: rgba(0, 0, 0, 0.2);
    }
    /* from-content
    -----------------------------------*/
    .from-content {
        position: fixed;
        top: 0;
        left: 12.4%;
        bottom: 0;
        margin: auto auto;
        width: 35%;
        max-width: 450px;
        height: 85%;
        padding: 1rem;
        box-sizing: border-box;
        background: #ffffff;
    }
    /* from-content  from-content-item
    -----------------------------------*/
    .from-content .from-content-item{
        width: 100%;
        height: 100%;
        overflow: auto;

    }
    .from-content-item::-webkit-scrollbar {
        display: none;
    }
    .from-content .item {
        color: #ffffff;
        font-size: 2rem;
        margin-bottom: 1.4rem;
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    }

    .from-content .item-head {
        width: 100%;
        background: #42b983;
        padding: 0.8rem 0;
        text-indent: 1.4rem;
    }
    .item-head .item-head-time{
        display: inline-block;
        text-align: right;
        font-size: 1.6rem;
        float: right;
        margin-top: 4px;
        margin-right: 1rem;
    }
    .item-head-time input{
        background: #42b983;
        border-bottom: 2px solid #ffffff;
        text-indent: 1rem;
        color: #ffffff;
    }
    .from-content .item-content {
        color: #313131;
        font-size: 1.6rem;
        margin: 1rem 1rem;
        line-height: 1.5;
    }

    .from-content .item-footer {
        width: 100%;
        background: #42b983;
        text-align: right;
    }
    .from-content .inp-short {
        width: 50%;
        float: left;
    }
    .inp-short input[type='text'] {
        border-bottom: 2px solid #42b983;
        text-indent: 1rem;
    }
    .from-content .inp-long{
        width: 100%;
    }
    .from-content .inp-long-more{
        line-height: 1.6;
    }
    .inp-long input[type='text'] {
        border-bottom: 2px solid #42b983;
        text-indent: 1rem;
        width: 100%;
    }
    .from-content .last-item{
        margin-bottom: 4.5rem;
    }
    .from-content .xs{
        position: absolute;
        top: 0;
        right: 0;
        width: 0;
        height: 0;
        border-top: 4rem solid #3ca777;
        border-right: 4rem solid #3ca777;
        border-bottom: 4rem solid transparent;
        border-left: 4rem solid transparent;
    }
    .from-content .xs2{
        position: absolute;
        top: 0;
        right: 0;
        width: 0;
        height: 0;
        border-top: 2rem solid #ffffff;
        border-right: 2rem solid #ffffff;
        border-bottom: 2rem solid transparent;
        border-left: 2rem solid transparent;
    }
    /* from-content from-box-footer
    -----------------------------------*/
    .from-content .from-box-footer{
        position: absolute;
        bottom:8px;
        left: 5px;
        width: 100%;
        height: 4rem;
        /*border-top: 1px solid #333333;*/
        background: #ebebeb;
        box-shadow: -4px 9px 8px 0 rgba(0, 0, 0, 0.2);
    }
    .from-box-footer .butt{
        position: absolute;
        right: 2rem;
        top: 0;
        bottom: 0;
        margin: auto 0;
        width: 6rem;
        height: 2.5rem;
        border-radius: 0.4rem;
        border: 1px solid #3ead7b;
        font-size: 2rem;
        color: #3ca777;
        text-align: center;
        line-height: 2.5rem;
    }
    .from-box-footer .butt:hover{
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);

    }
</style>