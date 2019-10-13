<template>
  <div class="header">
      <div class="Top">
        <div class="content">
        <div style="padding-top:6px">
            <div style="float:left">
              <a href="/" name="top" title="way to explore"><div class="Logo"></div></a>
            </div>
            <div class="search" style="float:left;margin-left:10px">
              <div class="qaba">
                  <input type="text" class="onsearch">
              </div>
            </div>
            <div class="top-right" style="float:right;height:38px">
              <a href="/" class="top">首页</a>
              &nbsp;&nbsp;&nbsp;
              <a href="/signup" class="top">注册</a>
              &nbsp;&nbsp;&nbsp;
              <a href="/signin" class="top">登录</a>
            </div>
        </div>
        </div>
      </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.top-right a{
      color: #556;
    text-decoration: none;
    line-height:38px
    
}
.qaba{
    width: 276px;
    height: 28px;
    background-size: 276px 28px;
    background-image: url(../assets/qbar_light@2x.png);
    background-repeat: no-repeat;
    display: inline-block;
}
.onsearch{
  border: none;
    width: 222px;
    height: 26px;
    margin: 0 0 2px 30px;
    background-color: transparent;
    font-family: "Helvetica Neue","Luxi Sans","DejaVu Sans",Tahoma,"Hiragino Sans GB",STHeiti!important;
    font-size: 14px;
    line-height: 16px;
    outline: 0;
}
.Logo{
  width: 94px;
  height:30px;
  background-image: url(../assets/logo.png);
  background-repeat: no-repeat;
    display: inline-block;
        background-size: 90px 30px;
}
.content{
  width: 1060px;
  margin:0 auto;
}
  .Top{
    width: 100%;
    height:44px;
    font-size:15px;
    font-weight: 500;
    padding: 0 20px 0 20px;
    border-bottom: 1px solid rgba(0,0,0,.22);
  }
</style>
