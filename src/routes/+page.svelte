<script lang="ts">
	import emblaCarouselSvelte from 'embla-carousel-svelte';
	import Autoplay from 'embla-carousel-autoplay';

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
	<h1 class="text-white text-5xl tracking-small text-center">Recent Projects</h1>
</div>

<div class="container mx-auto px-4 py-10">
	<div
		class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-2 gap-5 place-content-center"
	>
		<a href="/" class="block card card-hover bg-white rounded-lg shadow-lg">
			<div class="grid grid-cols-2 grid-flow-col">
				<div>
					<h1 class="text-primary-500 text-3xl tracking-small text-center pt-4 card-header">
						Recent Projects
					</h1>
					<p class="text-secondary-200 text-1xl tracking-smallpt-4 card-header">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
						incididunt ut labore et dolore magna aliqua. Dolor sit amet consectetur adipiscing elit
						ut. Feugiat nisl pretium fusce id velit ut tortor. Sit amet risus nullam eget. Maecenas
						volutpat blandit aliquam etiam erat velit scelerisque in dictum. Et egestas quis ipsum
						suspendisse ultrices gravida. Sodales ut eu sem integer vitae justo eget magna
						fermentum. Et odio pellentesque diam volutpat commodo sed egestas egestas fringilla.
						Senectus et netus et malesuada fames. Eros in cursus turpis massa tincidunt dui ut
						ornare. Amet aliquam id diam maecenas ultricies mi eget. Id semper risus in hendrerit
						gravida. Iaculis urna id volutpat lacus laoreet non curabitur gravida.
					</p>
					<footer class="p-4 flex justify-start items-center space-x-4">
						<small>Current</small>
					</footer>
				</div>
				<img class="justify-end rounded-r-md" src="phone-screen.png" alt="..." />
			</div>
		</a>

		<a href="/" class="block card card-hover bg-white rounded-lg shadow-lg">
			<div class="grid grid-cols-2 grid-flow-col">
				<div>
					<h1 class="text-primary-500 text-3xl tracking-small text-center pt-4 card-header">
						Recent Projects
					</h1>
					<p class="text-secondary-200 text-1xl tracking-smallpt-4 card-header">
						Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
						incididunt ut labore et dolore magna aliqua. Dolor sit amet consectetur adipiscing elit
						ut. Feugiat nisl pretium fusce id velit ut tortor. Sit amet risus nullam eget. Maecenas
						volutpat blandit aliquam etiam erat velit scelerisque in dictum. Et egestas quis ipsum
						suspendisse ultrices gravida. Sodales ut eu sem integer vitae justo eget magna
						fermentum. Et odio pellentesque diam volutpat commodo sed egestas egestas fringilla.
						Senectus et netus et malesuada fames. Eros in cursus turpis massa tincidunt dui ut
						ornare. Amet aliquam id diam maecenas ultricies mi eget. Id semper risus in hendrerit
						gravida. Iaculis urna id volutpat lacus laoreet non curabitur gravida.
					</p>
					<footer class="p-4 flex justify-start items-center space-x-4">
						<small>Current</small>
					</footer>
				</div>
				<img class="justify-end rounded-r-md" src="phone-screen.png" alt="..." />
			</div>
		</a>
	</div>
</div>

<hr class="!border-t-4" />

<div class="container mx-auto p-10">
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
				I'm Frazier Kyle, passionate about games and skilled in designing immersive worlds, levels,
				and environments. As a Developer and Designer at Nitric Concepts, I've programmed
				interactive levels and developed background systems for engaging gaming experiences while
				collaborated with Mojang and YouTubers to create popular maps and games. Additionally, I
				lead Miami University's Game Design Club, mentoring the future of game design.
			</p>
			<p class="mb-4 text-lg font-semibold">
				I am seeking computer science and game development opportunities for after college. I'm very
				proud to have worked several on excellent games with incredible people, including AlchyBox,
				Express Polar, Midnight Heist, MGDC Games.
			</p>
			<!-- Centered Button linking to your portfolio -->
			<a href="/portfolio" class="mt-4 btn variant-ghost-success">
				<p class="px-5">Visit Portfolio</p>
			</a>
		</div>

		<!-- Picture of you (right of the text) -->
		<div class="mt-5 md:mt-0 md:ml-4">
			<div class="relative">
				<img
					src="gdc-me.png"
					alt="Profile"
					class="w-64 h-64 rounded-full border-4 border-primary-500"
				/>
			</div>
		</div>
	</div>
</div>

<div class="bg-surface-700 p-4 my-12">
	<div class="container mx-auto md:w-2/3">
		<div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4">
			{#each logos as logo (logo)}
				<div class="p-4 flex items-center">
					<!-- Added 'flex' and 'items-center' classes -->
					<img src={logo} alt="Logo" class="w-full h-auto" />
				</div>
			{/each}
		</div>
	</div>
</div>

<footer class="bg-white rounded-lg shadow m-4 dark:bg-gray-800">
	<div class="w-full mx-auto max-w-screen-xl p-4 md:flex md:items-center md:justify-between">
		<span class="text-sm text-gray-500 sm:text-center dark:text-gray-400"
			>© 2023 <a href="https://flowbite.com/" class="hover:underline">Flowbite™</a>. All Rights
			Reserved.
		</span>
		<ul
			class="flex flex-wrap items-center mt-3 text-sm font-medium text-gray-500 dark:text-gray-400 sm:mt-0"
		>
			<li>
				<a href="/" class="mr-4 hover:underline md:mr-6">About</a>
			</li>
			<li>
				<a href="/" class="mr-4 hover:underline md:mr-6">Privacy Policy</a>
			</li>
			<li>
				<a href="/" class="mr-4 hover:underline md:mr-6">Licensing</a>
			</li>
			<li>
				<a href="/" class="hover:underline">Contact</a>
			</li>
		</ul>
	</div>
</footer>

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
