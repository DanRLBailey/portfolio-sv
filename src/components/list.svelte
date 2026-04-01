<script lang="ts">
	import type { Snippet } from 'svelte';

	type ListProps = {
		title: string;
		items?: string[];
		children?: Snippet;
	};

	let { title, items, children }: ListProps = $props();
</script>

<ul>
	{title}
	{#if items}
		{#each items as item}
			<li>{item}</li>
		{/each}
	{/if}
	{#if children}
		{@render children()}
	{/if}
</ul>
