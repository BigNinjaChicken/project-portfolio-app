<script lang="ts">
	import Youtube from 'svelte-youtube-embed';
	import FeatureCard_2 from '../../Feature-Card-2.svelte';

	import Prog1 from '$lib/portfolio/feature-1/image-2.png';
	import Prog2 from '$lib/portfolio/feature-1/image-1.png';
	import Prog3 from '$lib/portfolio/feature-1/image-4.png';
	import Prog4 from '$lib/portfolio/feature-1/image-3.png';
	import Prog5 from '$lib/portfolio/feature-1/image-5.png';

	import { Table, tableMapperValues } from '@skeletonlabs/skeleton';
	import type { TableSource } from '@skeletonlabs/skeleton';

	const demoVideo1: string = 'RG8Sua8vprQ';
	const demoVideo2: string = 'v5IXmLyw68g';

	const sourceData = [
		{ position: 1, catagory: 'Itch.io Page', desc: '<a href="https://bigninjachicken.itch.io/rounds-on-me" class="btn bg-gradient-to-br variant-gradient-secondary-tertiary" target="_blank">Itch Store Site</a>' },
		{ position: 2, catagory: 'My Role', desc: 'Solo Developer' },
		{ position: 3, catagory: 'Game Engine', desc: 'Unreal Engine 5.3 (UE5)' },
		{ position: 4, catagory: 'Number of Players', desc: '2-15 Players' },
		{ position: 5, catagory: 'Genre', desc: 'Casual, Party Game, Multiplayer' },
		{ position: 6, catagory: 'Web App', desc: 'SvelteKit hosted on Render' }
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
				>Rounds On Me</span
			>
		</h1>
		<h2 class="text-surface-400 text-3xl tracking-small text-center" id="recent-projects">
			A Drinking Party Game.
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
				Rounds On Me Short Trailer
			</h1>
			<p class="text-sm text-surface-300 mb-2">This is a gameplay demo video.</p>
			<Youtube id={demoVideo1} />
		</div>
	</div>

	<div
		class="container mx-auto flex flex-col px-5 md:px-40 py-12 md:flex-row items-center"
		id="demo"
	>
		<div>
			<h1 class="title-font sm:text-5xl text-3xl mb-2 font-bold text-surface-50">
				Full Game Demo Video
			</h1>
			<p class="text-sm text-surface-300 mb-2">
				This gameplay preview video includes explicit language (Suitable for audiences 18 and
				older).
			</p>
			<Youtube id={demoVideo2} />
		</div>
	</div>

	<h1 class="title-font sm:text-4xl text-3xl mb-5 font-bold text-surface-50 text-center">
		- Experience Breakdown -
	</h1>

	<section class="text-gray-600 body-font bg-surface-800">
		<div class="container mx-auto flex flex-col px-5 md:px-40 py-12 md:flex-row items-center">
			<div
				class="md:flex-grow md:w-1/2 lg:pl-10 lg:pr-12 md:pl-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 items-center text-center"
			>
				<h1 class="title-font sm:text-5xl text-3xl mb-4 font-bold text-surface-50">
					Phone 🤝 Unreal
				</h1>
				<div class="mt-5 mb-8 text-lg">
					<p class="text-surface-100">
						In crafting a dynamic party game, accessibility is key. It's about making sure everyone,
						regardless of their tech-savviness, can jump right in and feel confident.
					</p>
					<p class="text-surface-100 mt-8">
						To achieve this, I devised a solution using Unreal Engine 5 (UE5) that seamlessly
						connects to the web. Imagine it like a website talking to a server. With my setup, when
						a new game lobby is created in UE5, it automatically links up with my server through
						Websockets. This means anyone using the web version can easily join in. These lobbies
						operate independently, allowing for multiple games to run at once without one affecting
						the other, even if errors occur.
					</p>
					<p class="text-surface-100 mt-8">
						I've carefully selected a tech stack focused on efficiency. By integrating parallel
						rendering in Svelte and employing optimized coding techniques, I ensure real-time data
						transmission. This means players get instant feedback for every move they make,
						heightening their gaming experience and providing timely guidance, particularly for
						newcomers.
					</p>
				</div>
			</div>
			<div class="w-full md:w-2/5 mt-0 sm:mt- md:mt-0">
				<img class="object-cover object-center rounded" alt="..." src={Prog2} />
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
			<div class="w-full md:w-2/5 mt-8 md:mt-0">
				<img class="object-cover object-center rounded" alt="tip_book" src={Prog1} />
			</div>
			<div
				class="mt-2 md:flex-grow md:w-1/2 lg:pl-10 lg:pr-12 md:pl-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 items-center text-center"
			>
				<h1 class="title-font sm:text-5xl text-3xl mb-4 font-bold text-surface-50">
					Merging Drinking And Video Games
				</h1>
				<div class="mt-5 mb-8">
					<p class="text-surface-100 text-lg">
						In the early development phase, I experimented with a unique twist on party game
						dynamics. Rather than penalizing the lowest-ranked player with a shot, as is common, I
						flipped the script.
					</p>
					<p class="text-surface-100 text-lg mt-8">
						Instead, I introduced a system where players could nominate a competitor to take a shot.
						In exchange, the selected player would gain a point multiplier for the next round. This
						added a layer of friendly competition, injecting energy into the party atmosphere.
						Taking a drink became a strategic move, benefiting players who found themselves in the
						hot seat. The result? Both parties were satisfied—the shot-taker received a boost, while
						the chooser enjoyed some mischievous camaraderie among friends.
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
				<div class="mt-5 mb-8 text-xl">
					<h2 class="h2 text-surface-100 text-bold">1. Server Feedback</h2>
					<p class="text-surface-100 text-xl">
						Ensure that essential information is readily available to players so that they can stay
						updated on the remaining time they have to input their responses, which is periodically
						streamed to their devices. Additionally, the game features multiple "Ready Up" sections
						that dynamically check whether players have real-world tasks, like taking a shot, and
						stream their readiness status to the screen.
					</p>
				</div>
			</div>
			<div class="w-full md:w-3/5 mt-8 md:mt-0 mx-auto">
				<img class="object-cover object-center rounded" alt="..." src={Prog3} />
			</div>
			<div
				class="w-full mt-10 md:pl-16 md:items-start md:text-left mb-16 md:mb-0 items-center text-center mx-auto"
			>
				<div class="mt-5 mb-8 text-xl">
					<h2 class="h2 text-surface-100 text-bold">2. Encouraging Conversation</h2>
					<p class="text-surface-100 text-xl">
						The game is designed to be a team-based experience, where players are paired with new
						partners to collaboratively create a story within each act. Initially, players were
						assigned a single teammate for the entire game, and together, they crafted a "Mad-Lib"
						story. However, in response to feedback, I made adjustments to the system to provide a
						fresh teammate for each round. This was achieved by using weighted randomness to
						maintain fairness based on the scoreboard. This adjustment ensures that every player has
						the opportunity to work on various stories throughout a single game.
					</p>
				</div>
			</div>
			<div class="w-full md:w-3/5 mt-8 md:mt-0 mx-auto">
				<img class="object-cover object-center rounded" alt="..." src={Prog5} />
			</div>
			<div
				class="w-full mt-10 md:pl-16 md:items-start md:text-left mb-16 md:mb-0 items-center text-center mx-auto"
			>
				<div class="mt-5 mb-8 text-xl">
					<h2 class="h2 text-surface-100 text-bold">3. Mathematically Interesting</h2>
					<p class="text-surface-100 text-xl">
						I wanted the game to feature a three-act sequence similar to how a magician performs a
						trick: retention ➜ retention ➜ reveal. In each round of the game, a score is stored for
						each sentence created in the story, determined by how players rate each other's
						contributions. As the game progresses, the system learns more about which story contains
						the funniest elements. So, in the final act of the game, the narrator recounts the
						highest-scoring story that players have collaboratively crafted, incorporating a bit of
						everyone's input.
					</p>
				</div>
			</div>
			<div class="w-full md:w-3/5 mt-8 md:mt-0 mx-auto">
				<img class="object-cover object-center rounded" alt="..." src={Prog4} />
			</div>
		</div>
	</section>

	<div class="container mx-auto md:flex-row px-5 md:px-40 py-5 items-center">
		<div class="card">
			<div
				class="w-full mt-10 md:pl-16 md:items-start md:text-left mb-16 md:mb-0 items-center text-center mx-auto py-5"
			>
				<div class="mt-5 mb-8 text-xl">
					<h2 class="h2 text-surface-100 text-bold">GitHub Repositories</h2>
					<p class="text-surface-100 text-xl font-bold">Rounds On Me Related:</p>
					<p class="text-surface-100 text-xl">
						<a
							href="https://github.com/BigNinjaChicken/PartyGameOne"
							class="hover:text-blue-600 visited:text-purple-300 ..."
							target="_blank"
						>
							Unreal Engine Game Repo
						</a>
					</p>
					<p class="text-surface-100 text-xl">
						<a
							href="https://github.com/BigNinjaChicken/party-game-one"
							class="hover:text-blue-600 visited:text-purple-300 ..."
							target="_blank"
						>
							Web App Repo
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
			<div class="md:px-40"><FeatureCard_2 /></div>
		</div>
		<div class="flex justify-center">
			<a href="/portfolio" class="mt-6 p-3 btn variant-ghost-success">
				<p class="px-10 text-lg">See All Projects</p>
			</a>
		</div>
	</div>
</main>
