<template>
	<div id="tab-bar">
		<slot></slot>
	</div>
</template>

<script>
	export default{
		name:'TabBar'
	}
</script>
<style scoped>
	
	
	#tab-bar{
		background-color:#f6f6f6;
		position: fixed;
		left:0;
		right:0;
		bottom: 0;
		display: flex;
	}
</style>