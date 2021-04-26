<template>
	<view>
		<!-- 个人中心的一些设置-->
		<!-- 头像名称以及等级 -->
		<view class="userInfo">
			<image class="userImg" src="../../static/logo.png" mode=""></image>
			<view class="userDetail">
				<view class="userName">
					小九咔咔
				</view>
				<view class="lv">
					LV7
				</view>
			</view>
		</view>
		<!-- 我的菜单 我的图书 待还图书 排行榜 -->
		<view class="meMenu">
			<view class="meBooks list">
				<image  src="../../static/logo.png" mode=""></image>
				<view class="">
					我的图书
				</view>
			</view>
			<view class="meReturn list">
				<image src="../../static/logo.png" mode=""></image>
				<view class="">
					待还图书
				</view>
			</view>
			<view class="ranking list">
				<image src="../../static/logo.png" mode=""></image>
				<view class="">
					达人排行
				</view>
			</view>
			<view class="integral list">
				<image src="../../static/logo.png" mode=""></image>
				<view class="">
					积分兑换
				</view>
			</view>
		</view>
		<!-- 其他类目菜单 -->
		<view class="otherMenu">
			<view class="otherList">
				<image src="../../static/logo.png" mode=""></image>
				<view class="">
					设置
				</view>
				<view class="">
					>
				</view>
			</view>
			<view class="otherList">
				<image src="../../static/logo.png" mode=""></image>
				<view class="">
					设置
				</view>
				<view class="">
					>
				</view>
			</view>
			<view class="otherList">
				<image src="../../static/logo.png" mode=""></image>
				<view class="">
					设置
				</view>
				<view class="">
					>
				</view>
			</view>
			<view class="otherList">
				<image src="../../static/logo.png" mode=""></image>
				<view class="">
					设置
				</view>
				<view class="">
					>
				</view>
			</view>
			<view class="otherList">
				<image src="../../static/logo.png" mode=""></image>
				<view class="">
					设置
				</view>
				<view class="">
					>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
		methods: {

		}
	}
</script>

<style scoped>
	.userInfo {
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.userImg {
		width: 200rpx;
		height: 200rpx;
		border-radius: 50%;
		margin: 20rpx 0;
	}

	.userDetail {
		text-align: center;
	}

	.meMenu {
		display: flex;
		justify-content: space-around;
		margin-top: 20rpx;
	}
	.meMenu image{
		width: 100rpx;
		height: 100rpx;
	}
	.meMenu .list{
		display: flex;
		flex-direction: column;
		align-items: center;
	}
	.otherMenu{
		margin-top: 20rpx;
	}
	.otherList{
		display: flex;
		height: 80rpx;
		align-items: center;
		background-color: #ccc;
		padding-left: 20rpx;
		position: relative;
	}
	.otherList image{
		width: 50rpx;
		height: 50rpx;
	}
	.otherList view:nth-child(2){
		margin-left: 20rpx;
	}
	.otherList view:nth-child(3){
		position: absolute;
		right: 50rpx;
	}
</style>
