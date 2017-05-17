<template>
  <div id="App">
    <h1>{{title}}</h1>
   <!-- 工具栏 -->
            <nav class="bar bar-tab">
                <a class="tab-item external active" href="#">
                    <span class="icon icon-home"></span>
                    <span class="tab-label">首页</span>
                </a>
                <a class="tab-item external" href="#">
                    <span class="icon icon-star"></span>
                    <span class="tab-label">收藏</span>
                </a>
                <a class="tab-item external" href="#">
                    <span class="icon icon-settings"></span>
                    <span class="tab-label">设置</span>
                </a>
    </nav>

  </div>
</template>

<script>
// require('!style-loader!css-loader!./css/sm.css/./css/sm.css');// 
// require("./css/sm.css");
import './js/zepto.js'
import './js/sm.js'
export default {
  
   data () {
    return {
      title: '测试入口'
      
    }
  },

  methods:{
   }
}
</script>
<style>
  
</style>


