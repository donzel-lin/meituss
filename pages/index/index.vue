<template>
	<view class="content">
		<view class="swiper-section">
			<uni-swiper-dot :info="info" :current="current"  field="content" :mode="mode">
				<swiper class="swiper-box" @change="change">
					<swiper-item v-for="(item ,index) in info" :key="index">
						<view class="swiper-item">
							{{item.content}}
						</view>
					</swiper-item>
				</swiper>
			</uni-swiper-dot>
		</view>

	</view>
</template>

<script>
	export default {
		data() {
			return {
				info: [{
					content: '内容 A'
				}, {
					content: '内容 B'
				}, {
					content: '内容 C'
				}],
				current: 0,
				mode: 'round',
			}
		},
		onLoad() {

		},
		methods: {
			change(e) {
				this.current = e.detail.current;
			}
		}
	}
</script>

<style lang="scss" scoped>
	.swiper-section {
		width: calc(100vw - 30upx);
		margin: 0 auto;
		border-radius: 10upx;
		background-color: #00ffee;
	}


</style>
