<script lang="ts">
	export type TimelineItem = {
		title: string;
		subtitle?: string;
		text?: string;
		date: string;
	};

	type TimelineProps = {
		items: TimelineItem[];
	};

	let { items }: TimelineProps = $props();
</script>

<div class="timeline">
	{#each items as item}
		<div class="timeline-item flex-col">
			<h3>{item.title}</h3>
			{#if item.subtitle}<h4>{item.subtitle}</h4>{/if}
			{#if item.text}<span>{item.text}</span>{/if}
			<span>{item.date}</span>
		</div>
	{/each}
</div>

<style lang="scss">
	.timeline {
		--border: var(--border-width) dashed var(--accent-color-1);

		display: grid;
		grid-template-columns: repeat(3, 1fr);
		grid-auto-flow: row dense;
		gap: var(--spacing);

		& > *:nth-child(6n + 3) {
			border-right: var(--border);
		}

		& > *:nth-child(6n + 4) {
			grid-column: 3;
		}

		& > *:nth-child(6n + 5) {
			grid-column: 2;
		}

		& > *:nth-child(6n + 6) {
			grid-column: 1;
			border-left: var(--border);
		}

		.timeline-item {
			border-top: var(--border);
			position: relative;
			padding-block-start: var(--spacing-2);
			padding-block-end: var(--spacing-2);
			padding-inline-start: var(--spacing);

			&::after {
				--width: 1.5rem;

				content: '';
				position: absolute;
				inset: 0;
				width: var(--width);
				height: var(--width);
				border-radius: var(--width);
				background-color: var(--background-color);
				border: var(--border-width) solid var(--accent-color-1);
				transform: translate(-50%, -50%);
				z-index: 1;
			}
		}
	}
</style>
