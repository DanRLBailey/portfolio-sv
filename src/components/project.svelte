<script lang="ts">
	import type { Link as LinkType } from '../types/link';
	import Link from './link.svelte';

	type ProjectProps = {
		title: string;
		text: string;
		links?: LinkType[];
		image: string;
	};

	let { title, text, links, image }: ProjectProps = $props();
</script>

<div class="project flex-row justify-between align-center">
	<div class="project-content flex-col">
		<h3>{title}</h3>
		<span class="text">{text}</span>
		{#if links}
			<div class="links flex-row">
				{#each links as link}<Link to={link.href} newTab>{link.title}</Link>{/each}
			</div>
		{/if}
	</div>
	{#if image}
		<img src={image} alt={title + '-image'} class="image" />
	{/if}
</div>

<style lang="scss">
	.project {
		gap: 4rem;

		&:nth-child(2n) {
			flex-direction: row-reverse;
		}

		.project-content {
			align-self: stretch;

			.text {
				font-size: 0.9rem;
				flex: 1;
			}

			.links {
				:global(a) {
					&:nth-child(3n + 1) {
						--color: var(--accent-color-1);
					}
					&:nth-child(3n + 2) {
						--color: var(--accent-color-2);
					}
					&:nth-child(3n + 3) {
						--color: var(--accent-color-3);
					}
				}
			}
		}

		.image {
			width: auto;
			height: 400px;
			aspect-ratio: 1.5 / 1;
			background-color: #bababa;
			object-fit: cover;
			object-position: center;
			transition: var(--transition);
			filter: grayscale(1);
			box-shadow: 0 0 50px rgba(0, 0, 0, 0.2);
		}

		&:hover {
			.image {
				filter: none;
			}
		}
	}
</style>
