<script lang="ts">
	export let image: string;
	export let text: string;
</script>

<div class="card">
	<img-wrapper>
		<img src={image} alt="Card Icon" />
	</img-wrapper>
	<div class="card-content">
		<p>{text}</p>
	</div>
</div>

<style lang="scss">
	.card-content {
		color: var(--color-text-light);
	}
</style>
