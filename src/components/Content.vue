<template>
    <div class="Wrapper">
      <div class="content">
        <Right/>
        <div class="main" style="width: auto;margin: 0 310px 0 20px;">
            <div style="height: 20px"></div>
            <div class="c-box" style="background-color: white;box-shadow: 0 2px 3px rgba(0,0,0,.1);border-bottom: 1px solid #e2e2e2;">
                <div class="c-inner">
                    <a v-for="i in headerData" :key="i.id" href=";" :class="[defaultVal== 'inner-'+i.id ? 'tab-click' : 'tab']">{{i.name}}</a>
                </div>
                <div class="c-inner-box">
                    <a href=";">酷工作</a>
                    <a href=";" class="mg5">求职</a>
                    <a href=";" class="mg5">职场话题</a>
                    <a href=";" class="mg5">外包</a>
                    <a href=";" class="mg5">公司评价</a>
                    <div style="float: right">
                        <a href=";" class="">发布我的简历</a>
                        <a href=";" class="mg5">发布招聘信息</a>
                    </div>
                </div>
            </div>
        </div>
      </div>
    </div>
</template>

<script>
import {headerData} from '../public/data.js'
import Right from '@/components/Right.vue'
export default {
  name: 'Content',
  props: {
    msg: String
  },
  created(){
    this.defaultVal = `inner-${this.random(1,10)}`;
    console.log(this.defaultVal)
  },
  data () {
    return {
      defaultVal: '',
      headerData
    }
   },
   methods:{
      random(lower, upper) {
        return Math.floor(Math.random() * (upper - lower+1)) + lower;
      } 
   },
   components: {
    Right
  }
  }
</script>

<style scoped>
  .mg5{
    margin-left: 10px;
  }
  .c-inner-box{
    background-color: #f9f9f9;
    padding: 10px 10px 10px 20px;
    font-size: 14px;
    line-height: 120%;
    text-align: left;
    border-bottom: 1px solid #e2e2e2;
  }
  .c-inner-box a{
    color: #778087;
    text-decoration: none;
    word-break: break-word;
    cursor: pointer;
  }
  .tab-click{
    display: inline-block;
    font-size: 14px;
    line-height: 14px;
    padding: 5px 8px 5px 8px;
    margin-right: 5px;
    border-radius: 3px!important;
    background-color: #334;
    color: #fff !important;
  }
  .c-inner{
    padding: 10px;
    font-size: 14px;
    line-height: 150%;
    text-align: left;
  }
  .c-inner a{
    display: inline-block;
    font-size: 14px;
    line-height: 14px;
    padding: 5px 8px 5px 8px;
    margin-right: 5px;
    color: #555;
    
  }
  .c-inner a:link{
    text-decoration: none;
    word-break: break-word;
  }
  .i-image1{
    margin: 0 auto;
    background-image: url(../assets/gd1.jpg);
    display: block;
    height: 135px;
    background-repeat: no-repeat;
    width: 250px;
  }
  .i-image{
    margin: 0 auto;
    background-image: url(../assets/gd2.jpg);
    display: block;
    height: 135px;
    background-repeat: no-repeat;
    width: 250px;
  }
  .normal.button {
    background-color: #fff;
    color: #333;
    text-shadow: 0 1px 0 #fff;
    text-decoration: none;
    font-weight: 700;
    margin-top:8px;
    box-shadow: 0 1px 0 rgba(66,66,77,.1);
}
.super.button {
    background-image: url(../assets/bg_blended_light.png);
    padding: 4px 8px 4px 8px;
    border: 1px solid rgba(80,80,90,.2);
    border-bottom-color: rgba(80,80,90,.35);
    border-radius: 3px;
    font-size: 14px;
    outline: 0;
}
  .r-box{
    background-color: white;
    box-shadow: 0 2px 3px rgba(0,0,0,.1);
    border-bottom: 1px solid #e2e2e2;
    margin-top: 20px
    
  }
  .cell{
    padding: 10px;
    font-size: 14px;
    line-height: 120%;
    text-align: left;
    border-bottom: 1px solid #e2e2e2;
    }
  
  .RightBar{
    width:270px;
    float: right;margin-right: 20px;
  }
  .content{
    min-width: 600px;
    max-width: 1100px;
    margin: 0 auto 0 auto;
  }
.Wrapper{
  background-color: #e2e2e2;
  background-image: url(../assets/shadow_light.png);
  background-repeat: repeat-x;
  min-height: 900px;
}
</style>
