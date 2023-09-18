<script>
	import InfoCard from '../components/info-card.svelte';
</script>

<section>
	<div class="intro-image-wrapper">
		<div class="intro-image-bg">
			<div class="intro-image-overlay" />
		</div>
		<div class="intro-image-content">
			<h1 class="intro-image-title">US Based Software Developers</h1>
			<p class="intro-image-subtitle">Your Source for On Demand Custom Software</p>
			<div class="button">
				<a href="/contact">
					<button class="btn btn-primary">Get Clarity On Your Project</button>
				</a>
			</div>
		</div>
	</div>
</section>
<section>
	<div class="info-container">
		<InfoCard image="images/team.svg" text="Custom Software Development" />
	</div>
</section>

<style lang="scss" scoped>
	.intro-image-wrapper {
		width: 100%;
		height: 500px;
		position: relative;

		.intro-image-bg {
			width: 100%;
			height: 100%;
			background: url('images/home-cover.jpg') no-repeat center center;
			background-size: cover;
			position: absolute;
			animation: zoomEffect 60s infinite alternate;

			@keyframes zoomEffect {
				from {
					transform: scale(1);
				}
				to {
					transform: scale(1.3);
				}
			}

			.intro-image-overlay {
				position: absolute;
				top: 0;
				left: 0;
				width: 100%;
				height: 100%;
				background-color: rgba(0, 0, 0, 0.5);
			}
		}

		.intro-image-content {
			position: absolute;
			top: 50%;
			left: 50%;
			transform: translate(-50%, -50%);
			text-align: center;

			.intro-image-title {
				font-size: 3.5rem;
				font-weight: 700;
				margin-bottom: 1rem;
				color: var(--color-primary);
			}

			.intro-image-subtitle {
				font-size: 2rem;
				font-weight: 600;
				color: var(--color-primary);
			}
		}
	}
</style>
