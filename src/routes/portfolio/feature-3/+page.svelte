<script lang="ts">
	import FeatureCard_1 from '../../Feature-Card-1.svelte';
	import Youtube from 'svelte-youtube-embed';
	import ArmoryAmusement from '$lib/portfolio/armory-amusement.png';
	import Maps from '$lib/portfolio/maps.gif';
	import Players from '$lib/portfolio/players.gif';
	import Group from '$lib/portfolio/group-pic.jpg';
	import Wardens from '$lib/portfolio/wardens.png';

	import { Table, tableMapperValues } from '@skeletonlabs/skeleton';
	import type { TableSource } from '@skeletonlabs/skeleton';

	const videoId1: string = 't75QsXLaVzo';

	const sourceData = [
		{
			position: 1,
			catagory: 'Itch.io Page',
			desc: '<a href="https://bigninjachicken.itch.io/pursuit-of-laughter" class="btn bg-gradient-to-br variant-gradient-secondary-tertiary" target="_blank">Itch Store Site</a>'
		},
		{ position: 2, catagory: 'Game Engine', desc: 'Unreal Engine 5.3 (UE5)' },
		{ position: 3, catagory: 'Number of Players', desc: '1-15 Player(s)' },
		{
			position: 4,
			catagory: 'Genre',
			desc: 'Rouge-Like, Story Game, Multiplayer'
		},
		{ position: 5, catagory: 'Online Subsystem', desc: 'Steam' }
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
				>Pursuit Of Laughter</span
			>
		</h1>
		<h2 class="text-surface-400 text-2xl tracking-small text-center" id="recent-projects">
			Kill for the Jester God.
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
				Pursuit Of Laughter Short Trailer
			</h1>
			<p class="text-sm text-surface-300 mb-2">This is a gameplay demo video.</p>
			<Youtube id={videoId1} />
		</div>
	</div>

	<section class="text-gray-600 body-font bg-surface-800">
		<div class="container mx-auto flex flex-col px-5 md:px-40 py-12 md:flex-row items-center">
			<div
				class="md:flex-grow md:w-1/2 lg:pl-10 lg:pr-12 md:pl-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 items-center text-center"
			>
				<h1 class="title-font sm:text-5xl text-3xl mb-4 font-bold text-surface-50">
					About the Game
				</h1>
				<div class="mt-5 mb-8 text-lg">
					<p class="text-surface-100">
						"Pursuit of Laughter" is developed by a dedicated team of six, under my leadership, with
						me handling all the programming aspects. In this captivating game, players assume the
						role of a lost soul resurrected by the Jester God. Tasked with returning to the Earth
						Realm, your mission is to collect souls on his behalf.
					</p>
					<p class="text-surface-100 mt-8">
						This journey will take you through various kingdoms where you must confront and defeat
						knights and sacred bosses. Each victory not only brings you closer to your goal but also
						strengthens your expanding arsenal of items, enhancing your abilities and preparing you
						for the challenges ahead.
					</p>
				</div>
			</div>
			<div class="w-full md:w-2/5 mt-0 sm:mt- md:mt-0">
				<img class="object-cover object-center rounded" alt="tip_book" src={ArmoryAmusement} />
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
				<img class="object-cover object-center rounded" alt="..." src={Maps} />
			</div>
			<div
				class="lg:flex-grow md:w-1/2 lg:pl-10 lg:pr-12 md:pl-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 items-center text-center"
			>
				<h1 class="mt-2 title-font sm:text-5xl text-3xl mb-4 font-bold text-surface-50">
					Level Creation
				</h1>
				<div class="mt-5 mb-8">
					<p class="text-surface-100 text-lg">
						In our new roguelike game, we merged randomized levels with controlled design for a fair
						yet challenging experience. I created a tool for precise block placement, influencing
						their orientation and determining boss encounter starting points, thus directing the
						player's journey through the game.
					</p>
					<p class="text-surface-100 text-lg mt-8">
						To improve multiplayer performance and minimize latency, each level is independently
						instantiated. I integrated scripts in each tile for flexible customization of key
						elements such as boss, player, enemy positions, level start points, and kill zones. This
						allows for precise tuning of the game's difficulty and playability.
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
					<h2 class="h2 text-surface-100 text-bold">1. Leading Programming With Teams</h2>
					<p class="text-surface-100">
						In my role as team leader and programmer, my primary goal was to maximize efficiency. To
						achieve this, I implemented a project management system using Trello, ensuring constant
						updates and seamless communication across the team. While developing the AI, I
						recognized the need for enemies to possess a basic punch capability. To address this, I
						designed a modular "Bite" component that could be easily integrated into any enemy
						class. Collaborating closely with our boss scripter, we evaluated its potential
						application. My approach to programming in a modular and abstract manner facilitated its
						effortless incorporation, enhancing our game's AI complexity and interaction dynamics.
					</p>
				</div>
			</div>
			<div class="w-full md:w-3/5 mt-8 md:mt-0 mx-auto">
				<img class="object-cover object-center rounded" alt="..." src={Group} />
			</div>
			<div
				class="w-full mt-10 md:pl-16 md:items-start md:text-left mb-16 md:mb-0 items-center text-center mx-auto"
			>
				<div class="mt-5 mb-8 text-lg">
					<h2 class="h2 text-surface-100 text-bold">Multiplayer Focus</h2>
					<p class="text-surface-100">
						I've always been passionate about multiplayer gaming, leading me to integrate component
						replication early in my projects. A challenge emerged when initiating dialogues with the
						'jester god' in playtests—either all players would enter the dialogue or only the server
						player would. I resolved this by making dialogues local actions and using a delegate to
						notify the server upon completion, smoothing the transition to the Earth raid. This
						adjustment significantly improved multiplayer synchronization and gameplay experience.
					</p>
				</div>
			</div>
			<div class="w-full md:w-3/5 mt-8 md:mt-0 mx-auto">
				<img class="object-cover object-center rounded" alt="..." src={Players} />
			</div>
			<div
				class="w-full mt-10 md:pl-16 md:items-start md:text-left mb-16 md:mb-0 items-center text-center mx-auto"
			>
				<div class="mt-5 mb-8 text-lg">
					<h2 class="h2 text-surface-100 text-bold">Enhancing Gameplay through Modular Design</h2>
					<p class="text-surface-100">
						In the game I developed, I implemented a comprehensive combat system that allows both
						allies and enemies to share items and abilities, enabling seamless integration across
						levels. This approach led to a significant improvement when playtesters expressed
						interest in using a spear-throwing ability initially exclusive to knight enemies. By
						leveraging the system's modularity, I adapted this feature for player use by adjusting
						parameters such as mesh models, particle effects, and values within the class blueprint,
						thus enriching the gameplay experience by incorporating the "Spear Spit" ability into
						the player's arsenal.
					</p>
				</div>
			</div>
			<div class="mx-auto w-full md:w-3/5 mt-8 md:mt-0">
				<img class="object-cover object-center rounded" alt="..." src={Wardens} />
			</div>
		</div>
	</section>

	<div class="container mx-auto md:flex-row px-5 md:px-40 py-5 items-center">
		<div class="card">
			<div
				class="w-full mt-10 md:pl-16 md:items-start md:text-left mb-16 md:mb-0 items-center text-center mx-auto py-5"
			>
				<div class="mt-5 mb-8 text-xl">
					<h2 class="h2 text-surface-100 text-bold">GitHub Repositorie</h2>
					<p class="text-surface-100 text-xl">
						<a
							href="https://github.com/BigNinjaChicken/ProjectCompany"
							class="hover:text-blue-600 visited:text-purple-300 ..."
							target="_blank"
						>
							Unreal Engine Game Repo
						</a>
					</p>
				</div>
			</div>
		</div>
	</div>

	<div class="container mx-auto p-10">
		<h1 class="text-white text-4xl tracking-small text-center" id="recent-projects">
			Check Out My Other Projects...
		</h1>
	</div>

	<div class="container mx-auto py-10">
		<div class="grid grid-cols-1 sm:grid-cols-1 md:grid-cols-1 lg:grid-cols-1 gap-5">
			<div class="md:px-40"><FeatureCard_1 /></div>
		</div>
		<div class="flex justify-center">
			<a href="/portfolio" class="mt-6 p-3 btn variant-ghost-success">
				<p class="px-10 text-lg">See All Projects</p>
			</a>
		</div>
	</div>
</main>
