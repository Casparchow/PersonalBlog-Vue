<template>
    <div class="header">
        <a href="http://baidu.com"><img class="bloglogo" src="../assets/image/logo.png"></a>
        <div class="saying">
            <h3 class="word">如果你浪费了自己的年龄，那是挺可悲的。因为你的青春只能持续一点儿时间。</h3>
            <h3 class="name">——王尔基</h3>
        </div>
        
    </div>
</template>

<script>
    export default {
        name: 'header'
    }
</script>

<style>
    .header{
        width: 1200px;
        height: 120px;
        margin-left: 100px;
        margin-bottom: 30px;
        background-color: rgba(44, 62, 80, 1);
        position: relative;
    }
    .bloglogo{
        width: 650px;
        height: 120px;

    }
    .saying{
        width: 520px;
        height: 90px;
        position: absolute;
        top: 20px;
        right: 30px;
        font-size: 20px;
        color: #FFFFFF;
    }
    .word{
        width: 520px;
        height: 50px;
        margin: 0;
        text-indent: 2em;
        text-align:justify;
    }
    .name{
        width: 520px;
        height: 20px;
        margin: 0; 
        text-align: right;
    }
</style>