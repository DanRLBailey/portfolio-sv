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
			color: '#66a3ff'
		},
		{
			title: 'GitHub',
			href: 'https://github.com/DanRLBailey',
			color: '#c566ff'
		},
		{
			title: 'LinkedIn',
			href: 'https://www.linkedin.com/in/danrbailey/',
			color: '#ffc266'
		}
	];
</script>

<section>
	<h1>Daniel Bailey</h1>
	<h2>Web & Software Developer</h2>

	<div class="header-links flex-row justify-start">
		{#each headerLinks as link}
			<Link to={link.href} color={link.color} newTab>{link.title}</Link>
		{/each}
	</div>

	<button>View Projects</button>
</section>

<style lang="scss">
	.header-links {
		margin-block-end: var(--spacing);
	}
</style>
