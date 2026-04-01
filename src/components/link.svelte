<script lang="ts">
	import type { Snippet } from 'svelte';

	type LinkProps = {
		to: string;
		newTab?: boolean;
		children: Snippet;
		color?: string;
	};

	let { to, newTab, children, color }: LinkProps = $props();
</script>

<a
	href={to}
	target={newTab ? '_blank' : '_self'}
	rel={newTab ? 'noopener noreferrer' : ''}
	style={color && `--color: ${color}`}
>
	{@render children()}
</a>

<style lang="scss">
	a {
		--color: currentColor;

		border-bottom: var(--border-width) solid var(--color);
		color: var(--color);
		position: relative;
		transition: var(--transition);
		outline-offset: var(--border-width);

		&::after {
			content: '';
			position: absolute;
			inset: 0;
			transform: scaleY(0);
			transform-origin: bottom;
			background-color: var(--color);
			transition: var(--transition);
		}

		&:hover,
		&:focus {
			&::after {
				transform: scaleY(0.15);
			}
		}
	}
</style>
