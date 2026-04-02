<script lang="ts">
	import type { Snippet } from 'svelte';

	type ListProps = {
		title: string;
		items?: string[];
		children?: Snippet;
		className?: string;
	};

	let { title, items, children, className }: ListProps = $props();
</script>

<div class="list-wrapper">
	<h3>{title}</h3>
	<ul class="list">
		{#if items}
			{#each items as item}
				<li>{item}</li>
			{/each}
		{/if}
		{#if children}
			{@render children()}
		{/if}
	</ul>
</div>

<style lang="scss">
	.list-wrapper {
		flex: 1;
		border-top: var(--border-width) solid var(--border-color);
		border-bottom: var(--border-width) solid var(--border-color);
		padding: var(--spacing);

		&:first-of-type {
			border-color: var(--accent-color-1);
		}
		&:nth-of-type(2) {
			border-color: var(--accent-color-2);
		}
		&:last-of-type {
			border-color: var(--accent-color-3);
		}

		h3 {
			background-color: var(--background-color);
			width: fit-content;
			padding-inline: var(--spacing);
			margin-block-start: calc((1rem + var(--spacing)) * -1);
			margin-inline-start: var(--spacing);
		}

		.list {
			list-style-type: none;
			margin: 0;
			padding-inline: var(--spacing-2);
		}
	}
</style>
