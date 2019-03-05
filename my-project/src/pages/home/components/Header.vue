<template>
<div class="header">
        <div class="header-left">
            <span class="iconfont">&#xe624;</span>
        </div>
        <div class="header-input">
            <span class="iconfont">&#xe632;</span>输入城市/景点/游玩主题
        </div>
        <div class="header-right">城市<span class="iconfont">&#xe64a;</span></div>
</div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>
<style  scoped>
    .header{
        background: #00bcd4;
        line-height: 0.86rem;
        color: #fff;
        display: flex;
    }
    .header-left{
        width: 0.64rem;
        float: left;
    }
    .header-left .iconfont{
        text-align: center;
        font-size: 0.4rem;
    }
    .header-input{
        flex: 1;
        background: white;
        margin-left: 0.2rem;
        height: 0.64rem;
        line-height: 0.64rem;
        border-radius: 0.1rem;
        margin-top: 0.12rem;
        color:#ccc;
    }
    .header-right{
        width: 1.24rem;
        float: right;
        text-align: center;
    }
    .header-right .iconfont{
        font-size: 0.24rem;
    }
</style>
