<script lang="ts">
	export let image: string;
	export let alt: string;
	export let title: string;
	export let problem: string;
	export let results: string[];
	export let solutions: { title: string; description: string }[];
</script>

<div class="card">
	<h1>{title}</h1>
	<div class="img-wrapper">
		<img src={image} {alt} />
	</div>
	<div class="card-content">
		<div class="problem">
			<h3>Problem:</h3>
			<p>{problem}</p>
		</div>
		<div class="results">
			<h3>Results:</h3>
			<ul>
				{#each results as result}
					<li>{result}</li>
				{/each}
			</ul>
		</div>
		<div class="solution">
			<h3>Solution:</h3>
			<ul>
				{#each solutions as { title, description }}
					<li class="solution-item">
						<span class="title">{title}:</span> <span>{description}</span>
					</li>
				{/each}
			</ul>
		</div>
	</div>
</div>

<style lang="scss">
	.card {
		padding: 3rem;
		display: flex;
		flex-direction: column;
		height: 100%;
		gap: 1rem;
		color: var(--color-text-light);
		background-color: #030a1a;
		font-size: 1.2rem;
		.img-wrapper {
			height: 400px;
			display: flex;
			justify-content: center;
			align-items: center;
			margin-bottom: 2rem;
			img {
				height: 100%;
				width: auto;
			}
		}
		.solution {
			.title {
				font-weight: 700;
			}
		}
	}
</style>
