<script lang="ts">
	import FeatureCard_3 from '../../Feature-Card-3.svelte';
	import Youtube from 'svelte-youtube-embed';
	import Express from '$lib/portfolio/express-polar.png';
	import Train1 from '$lib/portfolio/feature-2/train-1.png';
	import Train2 from '$lib/portfolio/feature-2/train-2.png';

	import { Table, tableMapperValues } from '@skeletonlabs/skeleton';
	import type { TableSource } from '@skeletonlabs/skeleton';

	const videoId1: string = '5zOFjNZDToA';
	const videoId2: string = '2dG6JJ-lnZM';
	const demoVideo1: string = 'W1c0M_Db2-U';

	const sourceData = [
		{ position: 1, catagory: 'Game Engine', desc: 'Unreal Engine 5.1 (UE5)' },
		{ position: 2, catagory: 'Number of Players', desc: '1-2 Player(s)' },
		{
			position: 3,
			catagory: 'Genre',
			desc: 'Speed Based, Intense Rythem Game, Multiplayer, Minigame'
		},
		{ position: 4, catagory: 'Online Subsystem', desc: 'Epic Online Services (EOS)' }
	];

	const tableSimple: TableSource = {
		// A list of heading labels.
		head: ['Catagory', 'Description'],
		// The data visibly shown in your table body UI.
		body: tableMapperValues(sourceData, ['catagory', 'desc']),
		// Optional: The data returned when interactive is enabled and a row is clicked.
		meta: tableMapperValues(sourceData, ['catagory', 'desc'])
	};
</script>

<main class="pt-16">
	<div class="container mx-auto p-10 pb-2">
		<h1 class="text-white text-5xl tracking-small text-center" id="recent-projects">
			<span
				class="bg-gradient-to-br from-blue-500 to-cyan-300 bg-clip-text text-transparent box-decoration-clone"
				>Express: Polar</span
			>
		</h1>
		<h2 class="text-surface-400 text-2xl tracking-small text-center" id="recent-projects">
			Runaway in the Train.
		</h2>
	</div>

	<div class="container mx-auto p-5 pb-10 md:px-80 items-center">
		<h3 class="h3 p-2">Game Specifications</h3>
		<Table source={tableSimple} />
	</div>

	<div
		class="container mx-auto flex flex-col px-5 md:px-40 py-12 md:flex-row items-center"
		id="demo"
	>
		<div>
			<h1 class="title-font sm:text-5xl text-3xl mb-2 font-bold text-surface-50">
				Express: Polar Gameplay Trailer
			</h1>
			<p class="text-sm text-surface-300 mb-2">This is a gameplay demo video.</p>
			<Youtube id={demoVideo1} />
		</div>
	</div>

	<section class="text-gray-600 body-font bg-surface-800">
		<div class="container mx-auto flex flex-col px-5 md:px-40 py-12 md:flex-row items-center">
			<div
				class="md:flex-grow md:w-1/2 lg:pl-10 lg:pr-12 md:pl-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 items-center text-center"
			>
				<h1 class="title-font sm:text-5xl text-3xl mb-4 font-bold text-surface-50">
					Bringing a Train to Life
				</h1>
				<div class="mt-5 mb-8 text-lg">
					<p class="text-surface-100">
						Express Polar's hook was giving a multiplayer experience while combining the genres
						"Rhythm Game" and "Speed Running Game," resulting in an exhilarating fusion of music and
						competition. This unique blend allowed players to challenge their reflexes and
						coordination. Join me on this journey as I dive into the creative process, technical
						challenges, and design decisions that brought Express Polar to life in my portfolio.
					</p>
				</div>
			</div>
			<div class="w-full md:w-2/5 mt-0 sm:mt- md:mt-0">
				<img class="object-cover object-center rounded" alt="tip_book" src={Express} />
			</div>
		</div>
	</section>

	<div class="container mx-auto flex px-5 md:px-40 py-4 flex-row items-center">
		<p class="mt-5 mb-8 text-center">
			<span class="text-yellow-600 font-bold text-xl" />
		</p>
	</div>

	<section class="text-gray-600 body-font bg-surface-800">
		<div class="container mx-auto flex flex-col px-5 md:px-40 py-12 md:flex-row items-center">
			<div class="w-3/5">
				<Youtube id={videoId2} />
			</div>
			<div
				class="lg:flex-grow md:w-1/2 lg:pl-10 lg:pr-12 md:pl-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 items-center text-center"
			>
				<h1 class="mt-2 title-font sm:text-5xl text-3xl mb-4 font-bold text-surface-50">
					How do I plan randomness?
				</h1>
				<div class="mt-5 mb-8">
					<p class="text-surface-100 text-lg">
						In Express: Polar, I aimed to craft a distinct and engaging experience for every
						playthrough, all while adhering to the fundamental concept of speedrunning. To strike
						the right balance between challenge and predictability, a hallmark of speedrunning
						games, I employed several key strategies.
					</p>
					<p class="text-surface-100 text-lg mt-8">
						First and foremost, I leveraged template train assets, dynamically loading them in a
						cardinal direction. This approach eliminated any randomness that would lead to
						frustrating backtracking, enabling players to maintain a consistent sense of direction
						throughout their runs. To inject excitement and opportunities for skill expression, I
						introduced occasional turns in the game's path.
					</p>
				</div>
			</div>
		</div>
	</section>

	<div class="container mx-auto flex px-5 md:px-40 py-4 flex-row items-center">
		<p class="mt-5 mb-8 text-center">
			<span class="text-yellow-600 font-bold text-xl" />
		</p>
	</div>

	<section class="text-gray-600 body-font bg-surface-800">
		<div class="container mx-auto md:flex-row px-5 md:px-40 py-12 items-center">
			<div
				class="w-full mt-10 md:pl-16 md:items-start md:text-left mb-16 md:mb-0 items-center text-center mx-auto"
			>
				<div class="mt-5 mb-8 text-lg">
					<h2 class="h2 text-surface-100 text-bold">1. Talking Quick Time Events</h2>
					<p class="text-surface-100">
						Players often find it challenging to fully customize their gaming experience and adjust
						the difficulty level to their liking in the existing game.
					</p>
					<p class="text-surface-100 mt-2">
						To solved this problem by developing the C++ "Train Generator" that offers enhanced
						player agency. With this feature, players can tailor the difficulty level to their
						preference by customizing various aspects of the game. For example, in more challenging
						settings, the relentless train conductor's speed increases as time elapses, and the
						number of train segments grows. Additionally, the difficulty rating directly influences
						the frequency of turns encountered during gameplay, providing a dynamic and adaptable
						gaming experience that caters to individual player preferences.
					</p>
				</div>
			</div>
			<div class="w-full md:w-3/5 mt-8 md:mt-0 mx-auto">
				<img class="object-cover object-center rounded" alt="..." src={Train1} />
			</div>
			<div
				class="w-full mt-10 md:pl-16 md:items-start md:text-left mb-16 md:mb-0 items-center text-center mx-auto"
			>
				<div class="mt-5 mb-8 text-lg">
					<h2 class="h2 text-surface-100 text-bold">2. Better Together</h2>
					<p class="text-surface-100">
						I wanted to strengthen the bonds with my friends through video games, and I realized
						that for this game, it needed to be cooperative. So I implemented the EOS SDK (Epic
						Online Services Software Development Kit) using “Buckets” to control different playable
						lobbies, enabling players to start the game together and collaborate to reach the end of
						the train. Additionally, I made this project templatable, allowing me to easily
						incorporate the static EOS files I created for this project into future games, instantly
						making them multiplayer-enabled.
					</p>
				</div>
			</div>
			<div class="w-full md:w-3/5 mt-8 md:mt-0 mx-auto">
				<Youtube id={videoId1} />
			</div>
			<div
				class="w-full mt-10 md:pl-16 md:items-start md:text-left mb-16 md:mb-0 items-center text-center mx-auto"
			>
				<div class="mt-5 mb-8 text-lg">
					<h2 class="h2 text-surface-100 text-bold">3. Rythem Minigame</h2>
					<p class="text-surface-100">
						At times, train conductors interrupt your journey, necessitating participation in a
						Disney Sing-A-Long-inspired minigame. However, this minigame was initially limited to
						certain screen sizes, leading to an inconsistent user experience. To address this issue,
						I undertook two key initiatives. Firstly, I implemented precise calculations to
						dynamically reposition the bouncing ball above the text, ensuring compatibility with
						various screen sizes. Secondly, I introduced backend systems that accurately gauge your
						performance, measuring how closely you match the conductor's tempo. This solution
						enhances the minigame's accessibility and consistency across different devices, creating
						a more engaging user experience.
					</p>
				</div>
			</div>
			<div class="w-full md:w-3/5 mt-8 md:mt-0 mx-auto">
				<img class="object-cover object-center rounded" alt="..." src={Train2} />
			</div>
		</div>
	</section>

	<div class="container mx-auto p-10">
		<h1 class="text-white text-4xl tracking-small text-center" id="recent-projects">
			Check Out My Other Projects...
		</h1>
	</div>

	<div class="container mx-auto py-10">
		<div class="grid grid-cols-1 sm:grid-cols-1 md:grid-cols-1 lg:grid-cols-1 gap-5">
			<div class="md:px-40"><FeatureCard_3 /></div>
		</div>
		<div class="flex justify-center">
			<a href="/portfolio" class="mt-6 p-3 btn variant-ghost-success">
				<p class="px-10 text-lg">See All Projects</p>
			</a>
		</div>
	</div>
</main>
