<template>
  <div id="App">
   
<!--top轮播图片-->
<Swiper></Swiper>

  </div>
</template>

<script>
import Swiper from './components/Swiper.vue'
export default {
  
   data () {
    return {
     
      
    }

  },
  mounted:function () {
        //类似于jquery中的ready方法
        this.$nextTick(function () {
    
        })

    },
  methods:{
   },
    components:{Swiper}
}
</script>
<style>
  /*@import "./css/light7.css";*/
 /* @import "./css/indexTest.css";*/
</style>


