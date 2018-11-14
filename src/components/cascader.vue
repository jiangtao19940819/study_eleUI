<template>
	<div id="cascader">
		<el-row>
			<el-col :span="12">
				<el-cascader v-model="selected" :options="options" placeholder="朴素点击版">
					
				</el-cascader>
			</el-col :span="6">
			<el-col>
				<el-button icon="el-icon-search" @click="getSelected">点我</el-button>
			</el-col>
		</el-row>
		<el-row>
			<el-col :span="12">
				<el-cascader v-model="selected" :options="options" placeholder="朴素hover版" expand-trigger="hover">
					
				</el-cascader>
			</el-col :span="6">
			<el-col>
				<el-button icon="el-icon-search" @click="getSelected">点我</el-button>
			</el-col>
		</el-row>
		<el-row>
			<el-col :span="12">
				<el-cascader v-model="selected" :options="options" placeholder="只显示最后一级hover版" expand-trigger="hover" :show-all-levels="false">
					
				</el-cascader>
			</el-col :span="6">
			<el-col>
				<el-button icon="el-icon-search" @click="getSelected">点我</el-button>
			</el-col>
		</el-row>
		<el-row>
			<el-col :span="12">
				<el-cascader v-model="selected2" :options="options"  expand-trigger="hover">
					
				</el-cascader>
			</el-col :span="6">
			<el-col>
				<el-button icon="el-icon-search" @click="getSelected">点我</el-button>
			</el-col>
		</el-row>
		<el-row>
			<el-col :span="12">
				<el-cascader v-model="selected" :options="options"   change-on-select="true" :show-all-levels="false">
					
				</el-cascader>
			</el-col :span="6">
			<el-col>
				<el-button icon="el-icon-search" @click="getSelected">点我</el-button>
			</el-col>
		</el-row>
	</div>
</template>
<script>
	export default {
		name : "cascader",
		data(){
			return {
				selected2 : ["sex","address","salary"],
				options : [
					{
					  label:"男孩",
					  value:"boy",
					  children:[
					  	{
					  		label:"蒋滔",
					  		value:"jiangtoa",
					  		children:[
					  			{
					  				label:"地址",
					  				value:"address"
					  			},{
					  				label:"年龄",
					  				value:"age"
					  			},{
					  				label:"工作",
					  				value:"work"
					  			}

					  		]
					  	},{
					  		label:"付洪",
					  		value:"fuhong",
					  		children:[
					  			{
					  				label:"地址1",
					  				value:"addres1"
					  			},{
					  				label:"年龄1",
					  				value:"age1"
					  			},{
					  				label:"工作1",
					  				value:"work1"
					  			}

					  		]

					  	},{
					  		label:"谢少胜",
					  		value:"xieshaosheng",
					  		children:[
					  			{
					  				label:"地址2",
					  				value:"address2"
					  			},{
					  				label:"年龄2",
					  				value:"age2"
					  			},{
					  				label:"工作2",
					  				value:"work2"
					  			}

					  		]
					  	}
					  ]
					},{
					  label:"省份",
					  value:"province",
					  children:[
					  	{
					  		label:"p蒋滔",
					  		value:"pjiangtoa",
					  		children:[
					  			{
					  				label:"地址",
					  				value:"paddress"
					  			},{
					  				label:"年龄",
					  				value:"page"
					  			},{
					  				label:"工作",
					  				value:"pwork"
					  			}

					  		]
					  	},{
					  		label:"p付洪",
					  		value:"pfuhong",
					  		children:[
					  			{
					  				label:"p地址1",
					  				value:"paddres1"
					  			},{
					  				label:"p年龄1",
					  				value:"page1"
					  			},{
					  				label:"p工作1",
					  				value:"work1"
					  			}

					  		]

					  	},{
					  		label:"p谢少胜",
					  		value:"pxieshaosheng",
					  		children:[
					  			{
					  				label:"p地址2",
					  				value:"paddress2"
					  			},{
					  				label:"p年龄2",
					  				value:"page2"
					  			},{
					  				label:"p工作2",
					  				value:"pwork2"
					  			}

					  		]
					  	}
					  ]
					},{
						label:"工资",
					  value:"salary",
					  children:[
					  	{
					  		label:"s蒋滔",
					  		value:"sjiangtoa",
					  		children:[
					  			{
					  				label:"地址",
					  				value:"saddress"
					  			},{
					  				label:"年龄",
					  				value:"sage"
					  			},{
					  				label:"工作",
					  				value:"swork"
					  			}

					  		]
					  	},{
					  		label:"s付洪",
					  		value:"sfuhong",
					  		children:[
					  			{
					  				label:"s地址1",
					  				value:"saddres1"
					  			},{
					  				label:"s年龄1",
					  				value:"sage1"
					  			},{
					  				label:"s工作1",
					  				value:"sork1"
					  			}

					  		]

					  	},{
					  		label:"s谢少胜",
					  		value:"sxieshaosheng",
					  		children:[
					  			{
					  				label:"s地址2",
					  				value:"saddress2"
					  			},{
					  				label:"s年龄2",
					  				value:"sage2"
					  			},{
					  				label:"s工作2",
					  				value:"swork2"
					  			}

					  		]
					  	}
					  ]
					}
				]
			}
		},
		methods : {
			getSelected : function(){
				alert(this.selected);
			}
		}
	}
</script>