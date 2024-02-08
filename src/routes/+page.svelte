<script lang="ts">
	import emblaCarouselSvelte from 'embla-carousel-svelte';
	import Autoplay from 'embla-carousel-autoplay';
	import FeatureCard_1 from './Feature-Card-1.svelte';
	import FeatureCard_2 from './Feature-Card-2.svelte';
	import FeatureCard_3 from './Feature-Card-3.svelte';

	const autoplayOptions = {
		delay: 3000,
		playOnInit: true
	};

	let options = { loop: true };
	let plugins = [Autoplay(autoplayOptions)];

	let logos = [
		'nitric_concepts_white_oktwof.png',
		'Nationwide-logo.png',
		'miami-logo-horizontal-stacked.png'
	];
</script>

<main class="pt-16">
	<div class="embla" use:emblaCarouselSvelte={{ options, plugins }}>
		<div class="embla__container">
			<div class="embla__slide">
				<div class="relative h-screen m-3">
					<img
						class="absolute inset-0 h-full w-full object-cover rounded-3xl"
						src="stat-gpt.jpg"
						alt="..."
					/>
					<div
						class="absolute inset-0 h-full w-full bg-gradient-to-tr from-black to-transparent opacity-100 rounded-3xl"
					/>
					<div class="absolute inset-0 flex items-center justify-center">
						<div class="grid grid-flow-row auto-rows-max text-center">
							<h1 class="text-white text-8xl tracking-small">Hello!</h1>
							<h1 class="text-white text-4xl p-3 tracking-wider">I'M A PROGRAMMER</h1>
						</div>
					</div>
				</div>
			</div>
			<div class="embla__slide">
				<div class="relative h-screen m-3">
					<img
						class="absolute inset-0 h-full w-full object-cover rounded-3xl"
						src="action-slapstick.png"
						alt="..."
					/>
					<div
						class="absolute inset-0 h-full w-full bg-gradient-to-tr from-black to-transparent opacity-100 rounded-3xl"
					/>
					<div class="absolute inset-0 flex items-center justify-center">
						<div class="grid grid-flow-row auto-rows-max text-center">
							<h1 class="text-white text-4xl p-3 tracking-wider">GAME DEVELOPER</h1>
						</div>
					</div>
				</div>
			</div>
			<div class="embla__slide">
				<div class="relative h-screen m-3">
					<img
						class="absolute inset-0 h-full w-full object-cover rounded-3xl"
						src="dino.jpg"
						alt="..."
					/>
					<div
						class="absolute inset-0 h-full w-full bg-gradient-to-tr from-black to-transparent opacity-100 rounded-3xl"
					/>
					<div class="absolute inset-0 flex items-center justify-center">
						<div class="grid grid-flow-row auto-rows-max text-center">
							<h1 class="text-white text-4xl p-3 tracking-wider">INNOVATOR</h1>
						</div>
					</div>
				</div>
			</div>
		</div>
		<div class="absolute bottom-4 left-0 w-full flex justify-center gap-4">
			{#each logos as _, index}
				<div class="w-[30px] h-[30px] grid place-items-center">
					<div class="w-full h-[3px] bg-black rounded-[.25rem] bg-surface-500" />
				</div>
			{/each}
		</div>
	</div>

	<div class="container mx-auto p-10">
		<h1 class="text-white text-5xl tracking-small text-center" id="recent-projects">
			Recent Projects
		</h1>
	</div>

	<div class="container mx-auto py-10">
		<div class="grid grid-cols-1 sm:grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-5">
			<FeatureCard_1 />
			<FeatureCard_2 />
		</div>
		<div class="grid grid-cols-1 sm:grid-cols-1 md:grid-cols-1 lg:grid-cols-1 gap-5 mt-5">
			<FeatureCard_3 />
		</div>
		<div class="flex justify-center">
			<a href="/portfolio" class="mt-6 p-3 btn variant-ghost-success">
				<p class="px-10 text-lg">See All Projects</p>
			</a>
		</div>
	</div>

	<hr class="!border-t-4" />

	<div class="container mx-auto p-10" id="about-me">
		<h1 class="text-white text-5xl tracking-small text-center">About Me</h1>
		<h1 class="text-surface-500 text-2xl tracking-small text-center">
			Love games and rock climbing!
		</h1>
	</div>

	<div class="container mx-auto md:w-2/3">
		<div class="flex flex-col md:flex-row items-center justify-center mt-5">
			<!-- Text about you (left of the picture) -->
			<div class="md:w-2/4 md:pr-8 pr-4 pl-4 md:pl-0 flex flex-col items-center justify-center">
				<p class="mb-4 text-lg">
					I'm Frazier Kyle, passionate about games and skilled in designing immersive worlds,
					levels, and environments. As a Developer and Designer at Nitric Concepts, I've programmed
					interactive levels and developed background systems for engaging gaming experiences while
					collaborated with Mojang and YouTubers to create popular maps and games. Additionally, I
					lead Miami University's Game Design Club, mentoring the future of game design.
				</p>
				<p class="mb-4 text-lg font-semibold">
					I am seeking computer science and game development opportunities for after college.
				</p>
			</div>

			<!-- Picture of you (right of the text) -->
			<div class="mt-5 md:mt-0 md:ml-4">
				<div class="relative">
					<img
						src="gdc-me.png"
						alt="Profile"
						class="w-80 h-80 rounded-full border-4 border-primary-500"
					/>
				</div>
			</div>
		</div>
		<!-- Centered Button linking to your portfolio -->
		<div class="flex justify-center">
			<a href="/contacts" class="mt-4 p-4 btn variant-ghost-success">
				<p class="px-7 text-lg">My Resume</p>
			</a>
		</div>
	</div>

	<div class="bg-surface-700 p-4 my-12">
		<div class="container mx-auto md:w-2/3">
			<div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 place-items-center">
				{#each logos as logo (logo)}
					<div class="p-4 flex justify-center items-center">
						<img src={logo} alt="Logo" class="max-h-64 w-auto mx-auto" />
					</div>
				{/each}
			</div>
		</div>
	</div>
</main>

<style>
	.embla {
		overflow: hidden;
	}
	.embla__container {
		display: flex;
	}
	.embla__slide {
		flex: 0 0 100%;
		min-width: 0;
	}
</style>
