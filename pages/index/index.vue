<template>
	<view class="main">
		<!-- 这里是首页 放置轮播图 推荐借阅图书等-->
		<!-- 轮播图 -->
		<view class="swiper">
			<swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000">
				<swiper-item>
					<view class="swiper-item">广告图1</view>
				</swiper-item>
				<swiper-item>
					<view class="swiper-item">广告图2</view>
				</swiper-item>
			</swiper>
		</view>
		<!-- 热门图书 -->
		<view class="hotBook Z">
			<view class="title">
				热门图书
			</view>
			<view class="bookList">
				<!-- 图片 作者 所属者 城市 距离 -->
				<view class="item">
					<image src="../../static/logo.png" mode="" style="width: 200rpx;height: 200rpx;"></image>
					<view class="booksName">十萬個為什麼十萬個為什麼十萬個為什麼</view>
					<view class="author">作者：小九</view>
					<view class="city">城市：西安</view>
					<view class="users">归属者：小九</view>
					<view class="distance">距离：5.9KM</view>
				</view>
			</view>
		</view>
		<!-- 新闻咨询 -->
		<view class="news Z">
			<view class="title">
				新闻资讯
			</view>
			<view class="newList">
				<view class="item">
					<image src="../../static/logo.png" style="width: 200rpx;height: 200rpx;" mode=""></image>
					<view class="content">
						<view class="newsTitle">
							新闻标题
						</view>
						<view class="newsContent">
							新闻内容新闻内容
						</view>
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
				
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style scoped>
	.Z{
		padding: 10rpx;
	}
	.swiper{
		background-color: red;
	}
	.title{
		padding-left: 10rpx;
		border-left: 10rpx solid red;
		margin: 0 0 10rpx 0;
	}
	.hotBook .bookList .item view {
		font-size: 26rpx;
		max-width: 200rpx;
		overflow-x: hidden;
		white-space:nowrap;
		 text-overflow: ellipsis;
	}
	.newList .item{
		display: flex;
	}
	.newList .item .content{
		padding: 0 0 0 10rpx;
	}
</style>
