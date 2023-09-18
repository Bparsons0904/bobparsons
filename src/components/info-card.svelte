<script lang="ts">
	export let image: string;
	export let alt: string;
	export let title: string;
	export let text: string;
</script>

<div class="card">
	<div class="img-wrapper">
		<img src={image} {alt} />
	</div>
	<div class="card-content">
		<h1>{title}</h1>
		<p>{text}</p>
	</div>
</div>

<style lang="scss">
	.card {
		padding: 1rem;
		background-color: #030a1a;
		display: flex;
		flex-direction: column;
		height: 100%; // take full height within grid cell
		gap: 1rem;

		.img-wrapper {
			width: 250px;
			height: 200px;
			display: flex;
			justify-content: center;
			align-items: center;
			margin: auto;
			img {
				width: 100%;
				height: auto;
			}
		}

		.card-content {
			color: var(--color-text-light);
			flex: 1;
			display: flex;
			flex-direction: column;
			justify-content: flex-start; // ensures content starts from the top
			margin-bottom: -25px;
			h1 {
				margin-bottom: 1rem; // space between title and paragraph
			}

			p {
				font-size: 1.2rem;
				line-height: 1.35;
				letter-spacing: 0.5px;
				margin: 0; // remove default margin
			}
		}
	}
</style>
