<script lang="ts">
	import type { Link as LinkType } from '../types/link';
	import Link from './link.svelte';

	type ProjectProps = {
		title: string;
		text: string;
		demoLink?: LinkType;
		repoLink?: LinkType;
		image: string;
	};

	let { title, text, demoLink, repoLink, image }: ProjectProps = $props();
</script>

<div>
	<h3>{title}</h3>
	<span>{text}</span>
	{#if demoLink}<Link to={demoLink.href}>{demoLink.title}</Link>{/if}
	{#if repoLink}<Link to={repoLink.href}>{repoLink.title}</Link>{/if}
	{image}
</div>
