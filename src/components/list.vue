<template>
	<div>
		<el-row :gutter="20"  class="postGrid">

			<el-col v-for="(data,key) in postList" :key="key" :push="2" :span="20" class="post" shadow="always" >
				
				<h3>{{data.name}}</h3>
				<iframe class="frame" :src="data.url" frameborder="1" width="100%" height="100%"></iframe>
				
			</el-col>
		</el-row>
	</div>
</template>

<script>

	import {eventBus} from "../main";
	export default{
		component:{

		},
		data(){

			return{
				postList:[],

			}
		},
		created() {
			eventBus.$on("postAdd", (post) => {
				
				this.postList.push(post);
				
			});
		}

	}

</script>

<style scoped lang="scss">

.postGrid{
	.post
	{
		border-radius: 10px;
		overflow: hidden;
		box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
		margin:50px 0px;
		.frame{

			width: 100%;
			height: 500px;
		}
	}


}


</style>