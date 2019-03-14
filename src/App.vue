<template>
  <div id="app">		
  			<Input></Input>
  			<Checkbox></Checkbox>
  </div>
</template>

<script>
  import Checkbox from './components/Checkbox';
  import Input from './components/Input';
  

export default {
  name: 'app',
  components: {
  	Checkbox,
  	Input,
  
  }
}
</script>

<style lang="scss">
	#app{
		height: 300px;
		width: 400px;
		margin:100px auto;
	}
</style>
