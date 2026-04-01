<script lang="ts">
	export type TimelineItem = {
		title: string;
		subtitle?: string;
		text: string;
		date: string;
	};

	type TimelineProps = {
		items: TimelineItem[];
	};

	let { items }: TimelineProps = $props();
</script>

<div>
	{#each items as item}
		<div>
			{item.title}
			{item.subtitle}
			{item.text}
			{item.date}
		</div>
	{/each}
</div>
