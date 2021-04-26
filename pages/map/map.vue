<template>
	<view>
		<!-- 地图界面 根据地理位置找寻附近人图书-->
		<view class="map">
			<map style="width: 100%; height: 100vh;" :latitude="latitude" :longitude="longitude" :markers="covers">
			</map>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				id: 0, // 使用 marker点击事件 需要填写id
				title: 'map',
				latitude: 39.909,
				longitude: 116.39742,
				covers: [{
					latitude: 39.909,
					longitude: 116.39742,
					iconPath: '../../static/logo.png'
				}, {
					latitude: 39.90,
					longitude: 116.39,
					iconPath: '../../static/logo.png'
				}]
			}
		},
		methods: {

		}
	}
</script>

<style scoped>
	.map {
		width: 100%;
		height: 100%;
	}
</style>
