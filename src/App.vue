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

    body, html {
        width: 100%;
        height: 100%;
        padding: 0;
        margin: 0;
    }

    #app {
        width: 100%;
        height: 100%;
    }
</style>
