<template>
 
<!--top轮播图片-->
<div>
   <img id="moveImgs" :src="now" alt="">
   <img src="../Images/1.jpg" alt="">
</div>

</template>

<script>

export default {
  // import Store from './js/axios.min.js'
 

    data () {
    return {
    	pic:["./src/Images/1.jpg","./src/Images/2.jpg","./src/Images/3.jpg"],
      now:require("../Images/1.jpg")
      
    }

  },
  mounted:function () {
        //类似于jquery中的ready方法
        this.$nextTick(function () {
    		//this.getPic();
        })

    },
  methods:{
  	getPic:function(){

				
			var i=0;
				//alert(this.pic.data[0].url)
 				 var _this=this;
	 			setInterval(function(){

			        if(i>=_this.pic.length){
			        i=0;
		       		}
		       		 _this.now=_this.pic[i];
		       		 var element = document.getElementById('moveImgs');
				     element.src =  _this.now;
		       		console.log(_this.now);
		       		 i++;
		     },2000);
			
		}
   }
  
}
</script>
<style>

</style>