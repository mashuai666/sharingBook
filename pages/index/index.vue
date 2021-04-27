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
				<scroll-view class="scrollView" scroll-x="true" scroll-left="120" white-space='nowrap'>
					<view class="item" v-for="(item,index) in hotBooks" :key=item.id @click="navDetail(item.id,'hot')">
						<image :src=item.image mode="" style="width: 200rpx;height: 200rpx;"></image>
						<view class="booksName">{{item.name}}</view>
						<view class="author">作者：{{item.author}}</view>
					</view>
				</scroll-view>
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
				// 热门书籍信息
				hotBooks: [{
						id: 0,
						image: '../../static/logo.png',
						name: '十万个为什么',
						author: '小九'
					},
					{
						id: 1,
						image: '../../static/logo.png',
						name: '十万个为什么',
						author: '小九'
					},
					{
						id: 2,
						image: '../../static/logo.png',
						name: '十万个为什么',
						author: '小九'
					},
					{
						id: 3,
						image: '../../static/logo.png',
						name: '十万个为什么',
						author: '小九'
					},
					{
						id: 4,
						image: '../../static/logo.png',
						name: '十万个为什么',
						author: '小九'
					},
					{
						id: 5,
						image: '../../static/logo.png',
						name: '十万个为什么',
						author: '小九'
					}
				]
			}
		},
		onLoad() {

		},
		methods: {
			// 跳转热门书籍详情界面 @params 书籍ID  即将进入的页面类型：热门|普通
			navDetail(id, type) {
				// 跳转至详情界面并传递书籍id以及要打开的详情页类型
				uni.navigateTo({
					url: '../booksDetail/booksDetail?type=' + type + '&id=' + id
				})
			}
		}
	}
</script>

<style scoped>
	.Z {
		padding: 10rpx;
	}

	.swiper {
		background-color: red;
	}

	.title {
		padding-left: 10rpx;
		border-left: 10rpx solid red;
		margin: 0 0 10rpx 0;
	}

	.hotBook .bookList .scrollView {
		white-space: nowrap;
		width: 100%;
	}

	.hotBook .bookList .scrollView .item {
		display: inline-block;
		padding: 0 10rpx;
	}

	.hotBook .bookList .item view {
		font-size: 26rpx;
		max-width: 200rpx;
		overflow-x: hidden;
		white-space: nowrap;
		text-overflow: ellipsis;
	}

	.newList .item {
		display: flex;
	}

	.newList .item .content {
		padding: 0 0 0 10rpx;
	}
</style>
