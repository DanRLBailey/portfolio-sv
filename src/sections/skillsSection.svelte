<script>
	import List from '../components/list.svelte';
</script>

<section>
	<List
		title="Web"
		items={[
			'HTML',
			'React, Vue, SvelteKit',
			'JavaScript, TypeScript',
			'AWS, Terraform, Docker',
			'Vitest, Jest, xUnit, Selenium',
			'CSS, SASS',
			'REST'
		]}
	/>
	<List
		title="Software"
		items={['C#', '.Net Core, Framework', 'Java, Spring Boot', 'WebAPI', 'SQL', 'TDD, BDD', 'MVC']}
	/>
	<List title="Games" items={['C++', 'Unreal Engine 4', 'Unity 2D, 3D', 'PC, Console, Mobile']} />
</section>
