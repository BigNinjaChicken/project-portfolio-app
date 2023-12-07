<script lang="ts">
	import FeatureCard_2 from '../../Feature-Card-2.svelte';

	import Prog1 from '$lib/portfolio/feature-1/image-2.png';
	import Prog2 from '$lib/portfolio/feature-1/image-1.png';
	import Prog3 from '$lib/portfolio/feature-1/image-4.png';
	import Prog4 from '$lib/portfolio/feature-1/image-3.png';
	import Prog5 from '$lib/portfolio/feature-1/image-5.png';

	import { Table, tableMapperValues } from '@skeletonlabs/skeleton';
	import type { TableSource } from '@skeletonlabs/skeleton';

	const sourceData = [
		{ position: 1, catagory: 'Game Engine', desc: 'Unreal Engine 5.3 (UE5)' },
		{ position: 2, catagory: 'Number of Players', desc: '2-15 Players' },
		{ position: 3, catagory: 'Genre', desc: 'Casual, Party Game, Multiplayer' },
		{ position: 4, catagory: 'Web App', desc: 'SvelteKit hosted on Render' }
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
						The essence of a successful party game lies in its accessibility, ensuring that even
						those not well-versed in technology can easily engage and receive confirmation that
						they're on the right track.
					</p>
					<p class="text-surface-100 mt-8">
						To address this, I implemented a solution within Unreal Engine 5 (UE5) that enables
						seamless web connections, akin to how a website communicates with a server. When a new
						lobby is created in UE5, it automatically establishes a Websocket connection to my
						server, allowing anyone using the web application version to join in. These lobbies
						operate asynchronously, facilitating multiple concurrent games, and mitigating the
						impact of errors, should they occur, as they are isolated to individual lobbies.
					</p>
					<p class="text-surface-100 mt-8">
						I've leveraged a carefully chosen tech stack designed for efficiency, incorporating
						parallel rendering in Svelte, and optimized coding practices that prioritize real-time
						data transmission. This setup enables instantaneous feedback to players for every action
						they take, enhancing the overall gaming experience while ensuring that less experienced
						players receive prompt feedback on their actions.
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
				<img class="object-cover object-center rounded " alt="tip_book" src={Prog1} />
			</div>
			<div
				class="mt-2 md:flex-grow md:w-1/2 lg:pl-10 lg:pr-12 md:pl-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 items-center text-center"
			>
				<h1 class="title-font sm:text-5xl text-3xl mb-4 font-bold text-surface-50">
					Merging Drinking And Video Games
				</h1>
				<div class="mt-5 mb-8">
					<p class="text-surface-100 text-lg">
						In the early stages of development, I randomly selected a player from the bottom of the
						leaderboard to take a shot as a sort of penalty for not winning the previous rounds.
						However, this idea had its drawbacks. In most party games, drinking is often a
						consequence of losing a round or a way to hinder your performance when you're already
						falling behind. I decided to turn this concept on its head.
					</p>
					<p class="text-surface-100 text-lg mt-8">
						To achieve this, I allowed players to choose one of their competitors to take a shot,
						but in return, the selected player would receive a point multiplier for the next round.
						This encourages a bit of competitiveness among friends, keeping the party lively and
						transforming the act of taking a drink into a beneficial mechanic for players who were
						"unfortunate" enough to be chosen by their friends. This resulted in both parties being
						satisfied—the player who took a shot received a multiplier, and the person who made the
						choice had some mischievous fun among friends.
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

	<div class="container mx-auto p-10">
		<h1 class="text-white text-4xl tracking-small text-center" id="recent-projects">
			Check Out My Other Projects...
		</h1>
	</div>

	<div class="container mx-auto py-10">
		<div class="grid grid-cols-1 sm:grid-cols-1 md:grid-cols-1 lg:grid-cols-1 gap-5 flex">
			<div class="md:px-40"><FeatureCard_2 /></div>
		</div>
		<div class="flex justify-center">
			<a href="/portfolio" class="mt-6 p-3 btn variant-ghost-success">
				<p class="px-10 text-lg">See All Projects</p>
			</a>
		</div>
	</div>
</main>
