<template>
	<view class="detail">
		<view class="title">{{objData.title}}</view>
		<view class="content">{{objData.body}}</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		},
		onLoad() {
			
		},
		methods:{
			getDetail(){
				uni.request({
					url:"http://jsonplaceholder.typicode.com/posts/1",
					success:res=>{
						console.log(res)
						this.objData=res.data
					}
				})
			}
		}
	}
</script>

<style lang="scss">
.detail{
	padding: 30rpx;
	.title{
		font-size:46rpx;
		color:#000;
		padding-bottom:20rpx;
	}
	.content{
		font-size:30rpx;
		color:#666;
		padding-bottom:60rpx;
	}
}
</style>
