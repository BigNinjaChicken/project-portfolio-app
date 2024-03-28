<script lang="ts">
	import FeatureCard_1 from '../../Feature-Card-1.svelte';
	import Youtube from 'svelte-youtube-embed';
	import xr1 from '$lib/portfolio/xr1.webp';
	import xr2 from '$lib/portfolio/xr2.jpg';
	import xr3 from '$lib/portfolio/xr3.jpg';
	import xr5 from '$lib/portfolio/xr5.png';

	import { Table, tableMapperValues } from '@skeletonlabs/skeleton';
	import type { TableSource } from '@skeletonlabs/skeleton';

	const videoId1: string = 'zP6qHePyVs0';

	const sourceData = [
		{ position: 3, catagory: 'My Role', desc: 'Unreal Engineer & XR Live Crew' },
		{ position: 4, catagory: 'Engines', desc: 'Unreal Engine 5.3 (UE5) & Disguise' }
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
				>McVey Datascience Building XR Opening</span
			>
		</h1>
		<h2 class="text-surface-400 text-2xl tracking-small text-center pt-2" id="recent-projects">
			Bring the opening show to life by utilizing Design, New Technology, and Programming.
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
			<h1 class="title-font sm:text-5xl text-3xl mb-5 font-bold text-surface-50">
				Building Grand Opening Trailer
			</h1>
			<Youtube id={videoId1} />
		</div>
	</div>

	<section class="text-gray-600 body-font bg-surface-800">
		<div class="container mx-auto flex flex-col px-5 md:px-30 py-12 md:flex-row items-center">
			<div
				class="md:flex-grow md:w-1/2 lg:pl-10 lg:pr-12 md:pl-16 flex flex-col md:items-start md:text-left mb-16 md:mb-0 items-center text-center"
			>
				<h1 class="title-font sm:text-5xl text-3xl mb-4 font-bold text-surface-50">
					My Part In the Show
				</h1>
				<div class="mt-5 mb-8 text-lg">
					<p class="text-surface-100">
						I developed the main XR background for Miami's president, Gregory Crawford, for his
						keynote speech and collaborated on additional XR backdrops for the show. I also worked
						with the camera crew to ensure immersive experiences throughout the event, showcasing
						the XR stage technology's capacity to extend beyond the LED screens into real life.
					</p>
					<p class="text-surface-100 mt-8">
						My involvement enhanced my understanding of live production dynamics and client
						satisfaction. I crafted "special moments" for the audience, like when an effect I
						created expanded the Unreal Engine scene into an immersive expanse as the president
						gestured, emphasizing the technology's impressive capabilities.
					</p>
					<!-- <p class="text-surface-100 mt-8 text-sm italic">
						Began as a game jam (hackathon) game and continued improving the experience afterwards.
					</p> -->
				</div>
			</div>
			<div class="w-full md:w-3/5 mt-0 sm:mt- md:mt-0">
				<img class="object-cover object-center rounded" alt="tip_book" src={xr1} />
				<p class="text-surface-100 text-center text-sm italic">
					This is me standing infront of one of the scenes a couple of days before the show.
				</p>
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
				class="w-full md:pl-16 md:items-start md:text-left mb-16 md:mb-0 items-center text-center mx-auto"
			>
				<div class="mt-5 mb-8 text-lg">
					<h2 class="h2 text-surface-100 text-bold text-center">See More</h2>
					<p class="text-surface-100 text-center text-sm italic">
						Some of the shots I helped create for the show.
					</p>
				</div>
			</div>
			<div class="w-full md:w-4/5 mt-8 md:mt-0 mx-auto">
				<img class="object-cover object-center rounded" alt="..." src={xr2} />
			</div>
			<div
				class="w-full mt-10 md:pl-16 md:items-start md:text-left mb-16 md:mb-0 items-center text-center mx-auto"
			/>
			<div class="w-full md:w-4/5 mt-8 md:mt-0 mx-auto">
				<img class="object-cover object-center rounded" alt="..." src={xr3} />
			</div>
			<div
				class="w-full mt-10 md:pl-16 md:items-start md:text-left mb-16 md:mb-0 items-center text-center mx-auto"
			/>
			<div class="w-full md:w-4/5 mt-8 md:mt-0 mx-auto">
				<img class="object-cover object-center rounded" alt="..." src={xr5} />
			</div>
			<p class="text-surface-100 text-center text-sm italic">
				This image shows off the in camera set extentsion I helped bring to life.
			</p>
		</div>
	</section>

	<div class="container mx-auto md:flex-row px-5 md:px-40 py-5 items-center">
		<div class="card">
			<div
				class="w-full mt-10 md:pl-16 md:items-start md:text-left mb-16 md:mb-0 items-center text-center mx-auto py-5"
			>
				<div class="mt-5 mb-8 text-xl">
					<h2 class="h2 text-surface-100 text-bold">GitHub Repository</h2>
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
