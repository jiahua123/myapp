<template>
	<div class="checkbox">
		<form> 
			<label v-for="item in list" :key="item.num"><input type="checkbox" :checked="item.isok" @click="ckbox(item.num,item.isok)" />{{item.text}}</label> 
		</form> 
		<div>
			<span>复选框选择的值：</span><span>{{mykey}}</span>
		</div>
	</div>
</template>

<script>
	export default {
  			data(){
  			 return {
  				list:[
  				  {
                    text:'苹果',
                    num:1,
                    isok:true
                },{
                    text:'桃子',
                    num:2,
                    isok:false
             
                },{
                   text:'香蕉',
                    num:3,
                    isok:false
                    
                },
                {
                   text:'雪梨',
                    num:4,
                    isok:false
                    
                },
                {
                   text:'其他',
                    num:5,
                    isok:false
                    
                }
  				],
  				mykey:1
  			  }
  			},
  			methods:{
  				ckbox(id,isok){
					this.list.filter((item)=>{
						if(id==item.num){
							 item.isok=!isok;
							 this.mykey=item.num;
						}else{
							item.isok=false;
						}						
					})
  				}
  			},
			
		}
</script>

<style lang="scss">
	.checkbox{
		margin-top: 30px;
		>form{
			input{
				margin-left: 20px;
			}	
		}
		>div{
				margin: 20px 0 0 20px;
				
		}
	}
</style>