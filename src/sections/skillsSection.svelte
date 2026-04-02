<script>
	import List from '../components/list.svelte';
</script>

<section class="flex-row justify-between">
	<List title="Web">
		<h4>Languages</h4>
		<span>HTML, CSS, SASS, JavaScript, TypeScript</span>
		<h4>Frameworks</h4>
		<span>SvelteKit, React, Vue</span>
		<h4>Testing</h4>
		<span>Vitest, Jest, xUnit, Selenium</span>
		<h4>CI/CD</h4>
		<span>AWS, Terraform, Docker</span>
	</List>
	<List title="Software">
		<h4>Languages</h4>
		<span>C#, Java</span>
		<h4>Frameworks</h4>
		<span>.Net Core, .Net Framework, Spring Boot, MVC</span>
		<h4>Testing</h4>
		<span>TDD, BDD</span>
		<h4>Database</h4>
		<span>SQL, MySQL, Postgres</span>
	</List>
	<List title="Games">
		<h4>Languages</h4>
		<span>C#, C++</span>
		<h4>Engines</h4>
		<span>Unreal Engine 4, Unity</span>
		<h4>Platforms</h4>
		<span>PC, Console, Mobile</span>
	</List>
</section>

<style lang="scss">
	section {
		gap: 2rem;

		h4 {
			color: var(--font-color-2);
			font-size: 0.75rem;
		}

		span {
			margin-block-end: var(--spacing);
			display: block;
			font-size: 0.9rem;
		}
	}
</style>
