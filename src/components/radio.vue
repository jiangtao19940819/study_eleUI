<template>
	<div id="radio">
		<el-row>
			<el-col :span="8">
				<el-radio-group v-model="boy">
					<el-radio :label='1'>选择一</el-radio>
					<el-radio :label="2">选择二</el-radio>
					<el-radio :label="3">选择三</el-radio>
				</el-radio-group>
			</el-col>
			<el-col :span="3">
				<el-button @click="alertname"  icon="el-icon-check" type="success" size="small">点击</el-button>
			</el-col>
		</el-row>
		<el-row>
			<el-col :span="8">
				<el-radio-group v-model="boy" text-color="yellow" fill="red">
					<el-radio-button :label='1' >选择一</el-radio-button>
					<el-radio-button :label="2" >选择二</el-radio-button>
					<el-radio-button :label="3" >选择三</el-radio-button>
				</el-radio-group>
			</el-col>
			<el-col :span="3">
				<el-button @click="alertname"  icon="el-icon-check" type="success" size="small">点击</el-button>
			</el-col>
		</el-row>
		<el-row>
			<el-col :span="8">
				<el-radio-group v-model="boy">
					<el-radio :label='1' border>选择一</el-radio>
					<el-radio :label="2" border>选择二</el-radio>
					<el-radio :label="3" border>选择三</el-radio>
				</el-radio-group>
			</el-col>
			<el-col :span="3">
				<el-button @click="alertname"  icon="el-icon-check" type="success" size="small">点击</el-button>
			</el-col>
		</el-row>
	</div>
</template>
<script>
	export default {
		name : "radio",
		data(){
			return {
				boy : "jingtao"
			}
		},
		methods : {
			alertname : function(){
				alert(this.boy)
			}
		}
	}
</script>