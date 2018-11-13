<template>
	<div id="layout">
		<el-row>
			<el-col :span="8" class="content">文章</el-col>
			<el-col :span="8" class="content">知道</el-col>
		</el-row>
		<el-row>
			<el-col :span="6" class="content"></el-col>
			<el-col :span="6" :offset="4" class="content"></el-col>
		</el-row>
		<el-row>
			<el-col :span="24" class="content"></el-col>
		</el-row>
	</div>
</template>
<script>
	export default {
		name:"layout",
		data(){
			return {

			}
		}
	}
</script>
<style>
	.content {
		min-height:36px;
		background-color:yellow;
		border:1px solid red;
	}
</style>