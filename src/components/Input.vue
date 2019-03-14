<template>
	<div class="in">
		<input type="text" v-model="val" />
		<div>
			<span>输入框的值：</span><span>{{val}}</span>
		</div>
	</div>
</template>

<script>
	export default {
  			data(){
	 			return {
				val:''
	 			}
	 		},
		}
</script>

<style lang="scss">
		.in{
			margin: 20px;
			
			>div{
				margin-top: 20px;
			}
		}
</style>