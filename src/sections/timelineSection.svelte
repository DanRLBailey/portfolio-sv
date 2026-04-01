<script lang="ts">
	import Timeline, { type TimelineItem } from '../components/timeline.svelte';

	const items: TimelineItem[] = [
		{
			title: 'University',
			subtitle: 'Staffordshire University',
			text: 'Games Development',
			date: 'September 2016 - June 2020'
		},
		{
			title: 'BEP Systems',
			text: 'Graduate Developer',
			date: 'February 2021'
		},
		{
			title: 'OpenMoney',
			text: 'Developer',
			date: 'November 2022'
		},
		{
			title: 'Raytheon',
			text: 'Developer',
			date: 'July 2023'
		}
	];
</script>

<section>
	<Timeline {items} />
</section>
