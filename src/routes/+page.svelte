<script>
	import InfoCard from '../components/info-card.svelte';
</script>

<section>
	<div class="intro-image-wrapper">
		<div class="intro-image-bg">
			<div class="intro-image-overlay" />
		</div>
		<div class="intro-image-content">
			<h1 class="intro-image-title">Software Development Experts</h1>
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
			text="Your goals drive our approach. We engage closely with you, diving deep into your requirements. This collaboration ensures our solutions are effective and align with your budget. With a transparent strategy, we lay out timelines and milestones. And when it comes to billing, we offer both hourly rates or task-based pricing, tailoring to what suits your project best."
		/>
	</div>
</section>

<section class="different">
	<div class="side-image-wrapper">
		<img src="images/side-panel-image.png" alt="Documents feeding into a computer" />
	</div>
	<div class="content">
		<h1>A Different Experience</h1>
		<p>
			We're not just another development agency; we're a collective brought together by more than
			just our renowned skills and high-performance code. It's our genuine love for software
			development that binds us. This deep-rooted passion shines through in the resilient,
			efficient, and top-tier quality of our work. Beyond just writing code, our expertise spans a
			multitude of products, languages, and frameworks. Plus, we don't stop at development: we're
			with you every step of the way, offering comprehensive solutions including hosting,
			maintenance, and deployment, ensuring your software's seamless journey from conception to
			going live.
		</p>
		<div class="stack-list">
			<div class="inner-stack-list">
				<span>React</span>
				<span>PostgreSQL</span>
				<span>SCSS</span>
				<span>Flutter</span>
				<span>Laravel</span>
				<span>MongoDB</span>
				<span>Next</span>
				<span>Django</span>
				<span>Git</span>
				<span>Bootstrap</span>
				<span>Dart</span>
				<span>Vue</span>
				<span>TypeScript</span>
				<span>Tailwind CSS</span>
				<span>Redis</span>
				<span>GraphQL</span>
				<span>Python</span>
				<span>FastAPI</span>
				<span>JavaScript</span>
				<span>Go Lang</span>
				<span>Ruby on Rails</span>
				<span>Next.js</span>
				<span>Svelte</span>
				<span>DynamoDB</span>
				<span>Angular</span>
				<span>Express</span>
				<span>CSS</span>
				<span>C#</span>
				<span>Node</span>
				<span>HTML</span>
				<span>Material UI</span>
				<span>PHP</span>
				<span>SQLite</span>
				<span>Nuxt.js</span>
				<span>MySQL</span>
				<span>Flask</span>
			</div>
		</div>
	</div>
</section>

<section class="dont-do">
	<div class="content">
		<h1>What We Stand For (and What We Don't)</h1>
		<p>
			We're not just any development agency. We don't believe in one-size-fits-all solutions, nor in
			selling pre-packaged software that misses the mark. Cutting corners, compromising on quality,
			and overpromising only to underdeliver? That's not us.
		</p>
		<p>
			We're also not a marketing or design agency. We're specialists, and our expertise is in
			software development.
		</p>
		<p>
			What we do believe in is partnership. We're here to be your steadfast ally in the world of
			software, to truly understand your needs, and to provide solutions tailored to your vision,
			budget, and timeline. With us, it's personal. You're not just another client; you're a
			teammate.
		</p>
	</div>
	<div class="side-image-wrapper">
		<img src="images/side-image.svg" alt="Documents feeding into a computer" />
	</div>
</section>

<section class="contact">
	<a href="/contact"><button class="btn btn-cta">Contact Us</button></a>
	<a href="/about">
		<button class="btn btn-cta">Our Work</button>
	</a>
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
		gap: 4rem;
		padding: 2rem;

		@media (max-width: 768px) {
			grid-template-columns: 1fr;
		}
	}

	.different {
		margin: 4rem 0;
		display: grid;
		grid-template-columns: 2fr 3fr;
		align-items: center;
		justify-content: center;
		gap: 2rem;
		padding: 2rem;
		color: var(--color-text-light);
		.side-image-wrapper {
			width: auto;
			height: 300px;
			position: relative;
			overflow: hidden;
			img {
				width: 100%;
				height: 100%;
				position: absolute;
				top: 0;
				left: 0;
			}
		}
		.content {
			font-size: 1.2rem;
			line-height: 1.35;
			letter-spacing: 0.5px;
			overflow: hidden;
			.stack-list {
				position: relative;
				overflow: hidden;
				width: 100%;

				.inner-stack-list {
					display: flex;
					white-space: nowrap;
					animation: scroll 60s linear infinite;

					span {
						padding: 0 1.5em;
						border-right: 1px solid var(--color-primary);
					}
				}
			}
		}
	}

	.dont-do {
		display: grid;
		grid-template-columns: 3fr 2fr;
		align-items: center;
		justify-content: center;
		gap: 2rem;
		padding: 2rem;
		background-color: var(--color-secondary-dark);
		color: var(--color-text-light);
		.side-image-wrapper {
			width: auto;
			height: 300px;
			position: relative;
			overflow: hidden;
			img {
				width: 100%;
				height: 100%;
				position: absolute;
				top: 0;
				left: 0;
			}
		}
		.content {
			font-size: 1.2rem;
			line-height: 1.35;
			letter-spacing: 0.5px;
			overflow: hidden;
		}
	}

	.contact {
		padding: 2rem;
		display: flex;
		justify-content: space-evenly;
	}

	@keyframes scroll {
		0% {
			transform: translateX(100%);
		}
		100% {
			transform: translateX(-100%);
		}
	}
</style>
