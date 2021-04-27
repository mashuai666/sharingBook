<template>
	<view class="main">
		<!-- 书籍详情界面 -->
		<!-- <view class="" v-if="pageType=='hot'">
			热门
		</view> -->
		<!-- 上方图书信息显示 -->
		<view class="headerBookDetail">
			<view class="img">
				<image src="../../static/logo.png" mode=""></image>
			</view>
			<view class="rightContent">
				<view class="title">
					《十万个为什么》
				</view>
				<view class="info">
					十万个为什么简介十万个为什么简介十万个为什么简介十万个为什么简介十万个为什么简介十万个为什么简介
					查看更多
				</view>
				<view class="author">
					作者：小九
				</view>
				<view class="评分">
					<view class="star">
						星星
					</view>
					<view class="ido">
						我要评分
					</view>
				</view>
			</view>

		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				// 页面类型
				pageType: ''
			}
		},
		onLoad(e) {
			let id = e.id;
			switch (e.type) {
				case 'hot':
					this.pageType = e.type
					break;
				case 'normal':
					this.pageType = e.type
					break;
				default:
					uni.showToast({
						mask: true,
						icon: 'loading',
						title: '出错，返回中'
					})
					setTimeout(() => {
						uni.navigateBack({
							delta: 1
						})
					}, 1000)
					break;
			}
		},
		methods: {

		}
	}
</script>

<style scoped>
	.main {
		padding: 10rpx;
	}

	.headerBookDetail {
		display: flex;
	}

	.headerBookDetail .img image {
		width: 200rpx;
		height: 300rpx;
	}
</style>
