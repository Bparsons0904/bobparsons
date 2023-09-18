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
			<p class="intro-image-subtitle">Your Source for On Demand Software Solutions</p>
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
		<InfoCard
			image="images/who-we-are.svg"
			alt="Illistration of a team of developers"
			title="Who We Are"
			text="We're a dedicated team of developers, hailing from across the United States. Our collective expertise spans a vast range of software development niches, allowing us to tackle projects of any scale or complexity. Whether you need an individual specialist or a small team, we're adaptable and ready. Passionate about technology, we thrive on transforming your ideas into tangible, functioning realities."
		/>
		<InfoCard
			image="images/what-we-do.svg"
			alt="Illistration of a team of developers"
			title="What We Do"
			text="At the heart of our services lies the dedication to crafting tailored software solutions that cater to both businesses and individuals. Whether you're looking to start a new digital endeavor, enhance an existing platform with fresh features, or troubleshoot pesky bugs, we've got your back. Our expertise extends to stabilizing and optimizing current projects, ensuring your software runs smoothly and efficiently."
		/>
		<InfoCard
			image="images/how-we-work.svg"
			alt="Illistration of a team of developers"
			title="How We Work"
			text="Collaboration is at the core of our approach. We immerse ourselves in understanding your unique needs, ensuring that our solutions are not only effective but also budget-friendly. Together, we'll co-create a strategy that outlines clear timelines and milestones, providing a transparent roadmap tailored to your goals. Moreover, we offer flexible billing options: whether you prefer hourly rates or task-based pricing, we're here to accommodate your financial preferences."
		/>
	</div>
</section>

<style lang="scss" scoped>
	.intro-image-wrapper {
		width: 100%;
		height: 500px;
		position: relative;
		overflow: hidden;

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

	.info-container {
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		align-items: stretch; // ensuring all cards stretch to the tallest card's height
		justify-content: center;
		gap: 2rem;
		padding: 2rem;

		@media (max-width: 768px) {
			grid-template-columns: 1fr;
		}
	}
</style>
