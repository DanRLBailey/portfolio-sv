<script lang="ts">
	import Project from '../components/project.svelte';
	import MusicalChairsImage from '$lib/assets/images/musical-chairs.png';
	import KaraokeImage from '$lib/assets/images/karaoke.png';
	import MinesweeperImage from '$lib/assets/images/minesweeper.png';
	import VueCalendarImage from '$lib/assets/images/vue-calendar.png';
	import RhythmRunnerImage from '$lib/assets/images/rhythm-runner.png';
	import DlitasImage from '$lib/assets/images/dlitas.png';
	import FypImage from '$lib/assets/images/fyp.png';
	import TgpImage from '$lib/assets/images/tgp.png';
</script>

<section class="flex-col">
	<Project
		title="Musical Chairs"
		text="A project made in NextJS to help learn guitar songs. Shows a song's lyrics, chords & tabs, as well as their respective timings. Scrolls the song along with the music and highlights the relevant information"
		image={MusicalChairsImage}
		links={[
			{
				href: 'https://musicalchairs.dbailey.dev/',
				title: 'Demo'
			},
			{
				href: 'https://github.com/DanRLBailey/musical-chairs',
				title: 'Repo'
			}
		]}
	/>
	<Project
		title="Karaoke"
		text="React wrapper around YouTube karaoke videos. Fetches video meta information in the background at startup for optimised search, and fetches actual videos when added to queue. Mobile friendly for joining, desktop recommended for hosting"
		image={KaraokeImage}
		links={[
			{
				href: 'https://karaoke.dbailey.dev/',
				title: 'Demo'
			},
			{
				href: 'https://github.com/DanRLBailey/yt-karaoke-client',
				title: 'Repo (FE)'
			},
			{
				href: 'https://github.com/DanRLBailey/yt-karaoke',
				title: 'Repo (BE)'
			}
		]}
	/>
	<Project
		title="Minesweeper"
		text="Minesweeper, recreated in Sveltekit"
		image={MinesweeperImage}
		links={[
			{
				href: 'https://minesweeper.dbailey.dev/',
				title: 'Demo'
			},
			{
				href: 'https://github.com/DanRLBailey/svelte-sweeper',
				title: 'Repo'
			}
		]}
	/>
	<Project
		title="Vue Holiday Calendar"
		text="A Vue project that shows the best days to book holidays, based off bank holidays. Using the official National Holidays API, then calculates the best days from there"
		image={VueCalendarImage}
		links={[
			{
				href: 'https://daystobook.netlify.app//',
				title: 'Demo'
			},
			{
				href: 'https://github.com/DanRLBailey/days-to-book',
				title: 'Repo'
			}
		]}
	/>
	<Project
		title="Rhythm-Based Runner"
		text="Made in Unity and C#, with the intention of it being played on mobile devices. Features a portrait game screen and simple swipe controls. This build was completed in March 2020"
		image={RhythmRunnerImage}
		links={[
			{
				href: 'https://github.com/DanRLBailey/mobile-rhythm-runner',
				title: 'Repo'
			}
		]}
	/>
	<Project
		title="D'Litas"
		text="A cakes & catering company's ecommerce website. Made originally using HTML & CSS only, then later converted to be compatible with wordpress"
		image={DlitasImage}
		links={[
			{
				href: 'https://dlitas.netlify.app/',
				title: 'Demo'
			}
		]}
	/>
	<Project
		title="Final Year Project"
		text="The Final Year Project for University, made with a focus on accessibility for motor impaired players, predominantly by using single input controls. Controls consisted of buttons, microphones, and a range of other input devices that were planned. This build was completed in May 2020"
		image={FypImage}
		links={[
			{
				href: 'https://github.com/DanRLBailey/final-year-project',
				title: 'Repo'
			}
		]}
	/>
	<Project
		title="Manic Shooter"
		text="Made during the first 6 weeks of the second year of university in the TGP (Technical Games Production) module. Built in Unreal Engine 4 with mostly C++ and some blueprints"
		image={TgpImage}
		links={[
			{
				href: 'https://github.com/DanRLBailey/TGPSolo',
				title: 'Repo'
			}
		]}
	/>
</section>

<style lang="scss">
	section {
		gap: 10rem;
	}
</style>
