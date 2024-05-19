<template>
	<view class="">
		<!-- 配置路由 -->
		<u-tabbar :value="tabbarValue" @change="clickTabbar" :fixed="true" :placeholder="true"
			:safeAreaInsetBottom="true">
			<u-tabbar-item text="首页" icon="home"></u-tabbar-item>
			<u-tabbar-item text="厨房" icon="photo"></u-tabbar-item>
			<u-tabbar-item text="广场" icon="play-right"></u-tabbar-item>
			<u-tabbar-item text="我的" icon="account"></u-tabbar-item>
		</u-tabbar>
	</view>
</template>

<script setup>
	import {
		ref
	} from 'vue'
	let tabbarValue = ref('1');
	
	const clickTabbar = (e) => {
		console.log("click", e)
		if(e==1){
			uni.redirectTo({
				url: 'kitchen'
			});
		}
	}
	
</script>

<style>
</style>