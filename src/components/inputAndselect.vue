<template>
	<div id="is">
		<el-row>
			<el-col :span="18">
				<el-input placeholder="请输入查询内容-基础下拉框" clearable>
					<el-button slot="append" icon="el-icon-search"></el-button>
				</el-input>
			</el-col>
		</el-row>
		<el-row>
			<el-col :span="18">
				<el-select v-model="selected">
					<el-option v-for="item in items" :label = "item.label" :value = "item.value">
						
					</el-option>
				</el-select>
			</el-col>
			<el-col :span="6">
				<el-button @click="alertData" type="success" icon="el-icon-search">点击</el-button>
			</el-col>
		</el-row>
		<el-row>
			<el-col :span="18">
				<el-select v-model="selected" placeholder="请选择-可清空下拉框" clearable>
					<el-option v-for="item in items" :label = "item.label" :value = "item.value">
						
					</el-option>
				</el-select>
			</el-col>
			<el-col :span="6">
				<el-button @click="alertData" type="success" icon="el-icon-search">点击</el-button>
			</el-col>
		</el-row>
				<el-row>
			<el-col :span="18">
				<el-select v-model="selected" placeholder="请选择-可多选下拉框" clearable multiple>
					<el-option v-for="item in items" :label = "item.label" :value = "item.value">
						
					</el-option>
				</el-select>
			</el-col>
			<el-col :span="6">
				<el-button @click="alertData" type="success" icon="el-icon-search">点击</el-button>
			</el-col>
		</el-row>
		<el-row>
			<el-col :span="18">
				<el-select v-model="selected" clearable palceholder="分组下拉框">
					<el-option-group v-for="group in groups" :label="group.label" :value="group.value">
						<el-option v-for="item in group.options" :label="item.label" :value="item.value">
							
						</el-option>
					</el-option-group>
					
				</el-select>
			</el-col>
			<el-col :span="6">
				<el-button @click="alertData" type="success" icon="el-icon-search">点击</el-button>
			</el-col>
		</el-row>
	</div>
</template>
<script>
	export default {
		name : "inputAndselect",
		data(){
			return {
				items : [
					{label:"蒋滔",value:"24"},
					{label:"付洪",value:"25"},
					{label:"谢少胜",value:"26"}
				],
				groups : [
					{
						label:"姓名",
						value:"name",
						options:[
							{
								label:"蒋滔",
								value:"jiangtao"
							},{
								label:"付洪",
								value:"fuhong"
							},{
								label:"谢少胜",
								value:"xieshaosheng"
							}
						]
					},{
						label:"地址",
						value:"name",
						options:[
							{
								label:"北京",
								value:"beijing"
							},{
								label:"成都",
								value:"chengdu"
							},{
								label:"云南",
								value:"yunnan"
							}
						]
					}

				],
				selected : "100"
			}
		},
		methods : {
			alertData : function(){
				alert(this.selected);
			}
		}
	}
</script>