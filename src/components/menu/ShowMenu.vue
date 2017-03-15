<template>
    <div id="show-menu">
        <div class="menu-cont">
            <div class="logo"><i @click="kaClick" class="icon-camera-retro icon-4x"></i></div>
            <div class="file" @click="fileClick"><i class=" icon-file-alt icon-5x"></i></div>
        </div>
    </div>
</template>

<script type="text/ecmascript-6">
    export default{
        data(){
            return{
                msg:'hello vue'
            }
        },
        created(){

        },
        methods:{
            fileClick: function () {
                this.$emit('listenShowMenu',{"type":"fileClick","showFlag":true});
            },
            kaClick: function () {
                this.$emit('listenShowMenu',{"type":"kaClick"});
            }
        },
        components:{
           
        }
    }
</script>

<style>
    #show-menu{
        float: left;
        width: 8%;
        height: 100%;
        background: #ffffff;
     }
    .menu-cont{
        width: 90%;
        height: 99%;
        margin: 0 auto;
        padding-top: 1rem;
        box-sizing: border-box;
        box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
    }
    .logo , .file{
        width: 100%;
        color: #42b983;
        text-align: center;
        font-size: 1.2rem;
        margin-bottom: 1rem;
    }

</style>