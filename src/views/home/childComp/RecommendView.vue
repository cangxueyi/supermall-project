<template>
	<div id="recommendView">
		<div class="recommend" v-for="item in recommends">
			<a :href="item.link">
				<img :src="item.image" />
				<div>{{item.title}}</div>
			</a>
		</div>
	</div>
</template>

<script>
	export default {
		name:'RecommendView',
		props:{
			recommends:{
				type:Array,
				default(){
					return []
				}
			}
		}
	}
</script>

<style>
	#recommendView{
		display:flex;
		width:100%;
		font-size:12px;
		text-align:center;
		padding:10px 0 20px;
		border-bottom:8px solid #eee;
	}
	.recommend img{
		width:70px;
		height:70px;
		margin-bottom:10px;
	}
	.recommend{
		flex:1;
	}
</style>
