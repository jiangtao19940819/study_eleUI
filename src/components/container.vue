<template>
	<div id="container">
		<el-container class="position">
			<el-header class="content" line-height="60px"><i class="el-icon-edit
"></i></el-header>

			<el-container>
				<el-aside  width="100px" class="content">aside</el-aside>
				<el-container>
					<el-main class="content">main</el-main>
					<el-footer class="content" line-height="60px">footer</el-footer>
				</el-container>
			</el-container>
			
		</el-container>
	</div>
</template>
<script>
	export default {
		name:"container",

	}
</script>
<style>
	.content {
		background-color:yellow;
		border:1px solid red;
	}
	.position {
		position:absolute; 
		left:0; 
		top:0; 
		width:100%;
		height:100%;
	}
</style>