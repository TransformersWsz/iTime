<template>
	<view class="container">

		<view class="tui-content-box">
			<view class="tui-content">尊敬的用户，欢迎体验iTime！</view>
			<view class="tui-content">iTime是基于<u-link class="tui-content-email" href="https://github.com/dcloudio/hello-uniapp" text="uni-app"></u-link>框架开发的App。该App用于工业生产计时。主要的功能有秒表计次、数据操作（分析、复制、删除）等。</view>
			<view class="tui-content">App在使用过程中可能存在缺陷或者bug，您可以在
				<span class="tui-content-email" @tap="toFeedBack">
					问题反馈
				</span>
			里提供详细信息。</view>

			<view class="tui-content">
				或者以下方式联系我！
			</view>
			<view class="tui-content tui-content-email">邮箱：antcoder@outlook.com</view>

		</view>

	</view>
</template>

<script>
	export default {
		data() {
			return {}
		},
		methods: {
			toFeedBack() {
				uni.navigateTo({
					url: "/pages/my/feedback/feedback"
				})
			},
		}
	}
</script>

<style>
	.container {
		padding: 0 50rpx 40rpx 50rpx;
		box-sizing: border-box;
	}

	.tui-flex {
		display: flex;
		align-items: center;
		justify-content: center;
		padding-top: 40px;
	}


	@keyframes tui-go {
		0% {
			-webkit-transform: rotateX(0) rotateY(0);
			transform: rotateX(0) rotateY(0);
		}

		100% {
			-webkit-transform: rotateX(360deg) rotateY(360deg);
			transform: rotateX(360deg) rotateY(360deg);
		}
	}



	.tui-content-box {
		width: 100%;
		margin-top: 50px;
		padding: 30rpx;
		box-sizing: border-box;
		background-color: #fff;
		border-radius: 10rpx;
		box-shadow: 0 0 10rpx #eee;
	}

	.tui-content {
		color: #333;
		font-size: 30rpx;
		line-height: 44rpx;
		padding: 10rpx 0;
		text-align: justify;
	}

	.tui-content-email {
		color: #5677fc !important;
	}

	.tui-footer {
		display: flex;
		align-items: center;
		padding-top: 30rpx;
	}

	.tui-applets {
		width: 80px;
		height: 80px;
		display: block;
	}

	.tui-footer-text {
		font-size: 24rpx;
		color: #999;
		padding-left: 20rpx;
		width: 300rpx;
	}
</style>
