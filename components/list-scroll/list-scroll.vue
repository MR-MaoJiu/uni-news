<template>
	<view class="scroll">
		<scroll-view  class="list-scroll" scroll-y @scrolltolower="loadMore">
			<slot></slot>
		</scroll-view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		},
		methods: {
			loadMore() {
				this.$emit('loadmore')
			}
		}
	}
</script>

<style lang="scss">
	.scroll {
		flex:1;
		overflow: hidden;
		box-sizing: border-box;
		height: 100%;
		.list-scroll {
			height: 100%;
			display: flex;
			flex-direction: colum;
		}
	}
</style>
