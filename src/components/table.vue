<template>
	<div id="table">
		<!--<el-row>
			<el-col :span="18">
				<el-table :data="data" class="bd" style="width:80%">
					<el-table-column prop="name" label="姓名" class="bd"></el-table-column>
					<el-table-column prop="age" label="年龄"></el-table-column>
					<el-table-column prop="address" label="地址"></el-table-column>
				</el-table>
			</el-col>
		</el-row>
		<el-row>
			<el-col :span="18">
				<el-table :data="data" class="bd" style="width:80%" stripe>
					<el-table-column prop="name" label="姓名" class="bd"></el-table-column>
					<el-table-column prop="age" label="年龄"></el-table-column>
					<el-table-column prop="address" label="地址"></el-table-column>
				</el-table>
			</el-col>
		</el-row>-->
		<el-row>
			<el-col :span="18">
				<el-table :data="data" :row-class-name="tableRowClass" height="250">
					<el-table-column prop="name" label="姓名"></el-table-column>
					<el-table-column prop="age" label="年龄"></el-table-column>
					<el-table-column prop="address" label="地址"></el-table-column>
				</el-table>
			</el-col>
		</el-row>
		<el-row>
			<el-col :span="24">
				<el-table :data="data" :row-class-name="tableRowClass" height="250">
					<el-table-column fixed prop="name" label="姓名"></el-table-column>
					<el-table-column prop="age" label="年龄"></el-table-column>
					<el-table-column prop="address" label="地址"></el-table-column>
				</el-table>
			</el-col>
		</el-row>
	</div>
</template>
<script>
	export default {
		name : "table",
		data(){
			return {
				data : [
					{
						name : "蒋滔",
						age : "24",
						address : "北京"
					},
					{
						name : "付洪",
						age : "25",
						address : "云南"
					},
					{
						name : "谢少胜",
						age : "26",
						address : "南京"
					},
					{
						name : "严俊",
						age : "26",
						address : "成都"
					},
					{
						name : "王俊宇",
						age : "26",
						address : "伊犁"
					}
				]
			}
		},
		methods : {
			tableRowClass({row,rowIndex}){
				if(rowIndex===0){
					return 'warning-row';
				}
				else if(rowIndex===1){
					return 'success-row';
				}
				return ""
			}
		}
	}
</script>
<style>
	.bd {border:1px solid red}
	.el-table .warning-row {background: oldlace;}
	.el-table .success-row {background: #f0f9eb;}
</style>