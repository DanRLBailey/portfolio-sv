<script lang="ts">
	import Timeline, { type TimelineItem } from '../components/timeline.svelte';

	const items: TimelineItem[] = [
		{
			title: 'Staffordshire University',
			text: 'Games Development',
			date: 'September 2016'
		},
		{
			title: 'Finova',
			text: 'Graduate Developer',
			date: 'February 2021'
		},
		{
			title: 'OpenMoney',
			text: 'Full-stack Developer',
			date: 'November 2022'
		},
		{
			title: 'Raytheon',
			text: 'Full-stack Developer',
			date: 'July 2023'
		}
	];
</script>

<section>
	<Timeline {items} />
</section>
