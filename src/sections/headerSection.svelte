<script lang="ts">
	import type { Link as LinkType } from '../types/link';
	import Link from '../components/link.svelte';

	type HeaderLink = LinkType & {
		color: string;
	};

	const headerLinks: HeaderLink[] = [
		{
			title: 'CV',
			href: 'https://drive.google.com/file/d/1piQlVBi1FtH2EVaSmb6zkBNC6Cc3pHk0/view?usp=sharing',
			color: 'var(--accent-color-1)'
		},
		{
			title: 'GitHub',
			href: 'https://github.com/DanRLBailey',
			color: 'var(--accent-color-2)'
		},
		{
			title: 'LinkedIn',
			href: 'https://www.linkedin.com/in/danrbailey/',
			color: 'var(--accent-color-3)'
		}
	];
</script>

<section>
	<h1>Daniel Bailey</h1>
	<h2>Software Developer</h2>

	<div class="header-links flex-row justify-start">
		{#each headerLinks as link}
			<Link to={link.href} color={link.color} newTab>{link.title}</Link>
		{/each}
	</div>

	<button>View Projects</button>
</section>

<style lang="scss">
	.header-links {
		margin-block: calc(var(--spacing) * 2);
	}

	h2 {
		color: var(--font-color-2);
		font-size: 1.5rem;
	}
</style>
