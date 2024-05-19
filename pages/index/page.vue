<template>
	<view>
		<view class="">
			<span>{{dayStr}}</span>
		</view>
	</view>
</template>

<script setup>
import { onMounted, ref } from 'vue';
	const myTime=ref<Date>('2023-11-18')
	const dayStr =ref('')
	
	onMounted(()=>{
		dayStr.value=daysFromToday(myTime.value)
	})
	
	function daysFromToday(dateString) {
	  const today = new Date(); // 当前日期
	  const specifiedDate = new Date(dateString); // 指定日期
	  const millisecondsPerDay = 1000 * 60 * 60 * 24; // 每天的毫秒数
	 
	  // 计算时间差（毫秒）
	  const difference = today.getTime() - specifiedDate.getTime();
	 
	  // 计算差值的天数
	  return Math.round(difference / millisecondsPerDay)+1;
	}
</script>

<style>
</style>