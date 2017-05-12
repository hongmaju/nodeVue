 <<template>	
<div class="hello">
	<h1>{{msg}}</h1>
	<button v-on:click="onClickMe">click me!</button>
	<h1>{{msgfromfather}}</h1>
</div>
 </template>
 <script>
 	export	default{
 		data:function(){
 			return{
 				msg:'hello from component a',
 				msgTwo:'msgTwo'
 			}
 		},
 		props:['msgfromfather'],
 		methods:{
 			onClickMe:function(){
			// console.log(this.msgfromfather);
			this.$emit('child-tell-me-something',this.msg)
 			}
 		}
 	}

 </script>

 <style>
h1{
	color: #42b983;
}
 </style>
