<nav>
	<a href="/">Home</a>
	<a href="/about">About</a>
</nav>

<slot />

<style lang="scss">
	:global(body) {
		background-color: #000;
	}

	// Set root color variables
	:root {
		--color-primary: #fca311;
		--color-secondary-light: #e5e5e5;
		--color-secondary-dark: #14213d;
		--color-text-light: #ffffff;
		--color-text-dark: #000000;
	}

	:global(.btn) {
		padding: 1.5rem;
		border: 3px solid var(--color-primary);
		border-radius: 25px;
	}

	:global(.btn-primary) {
		font-size: 1.5rem;
		background-color: var(--color-secondary-dark);
		color: var(--color-text-light);
		transition: all 0.3s ease-in-out;
	}

	:global(.btn-primary:hover) {
		background-color: var(--color-primary);
		color: var(--color-text-dark);
	}
</style>
