<script lang="ts">
	import emblaCarouselSvelte from 'embla-carousel-svelte';
	import Autoplay from 'embla-carousel-autoplay';
	import ExpressPolar from '$lib/portfolio/express-polar.png';

	const autoplayOptions = {
		delay: 3500,
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
						src="dino.jpg"
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
						src="dino.jpg"
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
	</div>

	<div class="container mx-auto p-10">
		<h1 class="text-white text-5xl tracking-small text-center" id="recent-projects">
			Recent Projects
		</h1>
	</div>

	<div class="container mx-auto py-10">
		<div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-2 gap-5">
			<a href="/" class="block card card-hover shadow-lg h-min">
				<div class="flex items-center">
					<img class="w-1/2 m-5 pl-3" src="phone-screen.png" alt="..." />
					<div class="w-1/2 p-2 pl-0">
						<h1 class="text-primary-500 text-3xl tracking-small text-center card-header">
							AlchyBox - A Drinking Party Experience
						</h1>
						<p class="text-secondary-200 text-lg tracking-small pt-4 card-header">
							A party game developed in UE5, designed for 2 to 15 players, allows them to use their
							phones as controllers. Players collaborate to create ridiculous stories while
							challenging friends to take shots for multipliers.
						</p>
						<footer class="p-4 flex justify-center items-center space-x-4">
							<small>Current</small>
						</footer>
					</div>
				</div>
			</a>

			<a href="/" class="block card card-hover shadow-lg h-min">
				<div class="flex items-center">
					<img class="w-1/2 mx-4 pl-3" src="express-polar-thin.png" alt="..." />
					<div class="w-1/2 p-2 pl-0">
						<h1 class="text-primary-500 text-3xl tracking-small text-center card-header">
							Express: Polar
						</h1>
						<p class="text-secondary-200 text-lg tracking-small pt-4 card-header">
							I was the first-place winner in the MU Design Competition and my project was featured
							in the Miami Game Design Senior Project Fair. It's a UE5 multiplayer game created with
							C++ where players speedrun through a randomly generated series of minigames while
							being pursued by a crazed conductor.
						</p>
						<footer class="p-4 flex justify-center items-center space-x-4">
							<small>May, 2023</small>
						</footer>
					</div>
				</div>
			</a>
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
					I am seeking computer science and game development opportunities for after college. I'm
					very proud to have worked several on excellent games with incredible people, including
					AlchyBox, Express Polar, Midnight Heist, MGDC Games.
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
