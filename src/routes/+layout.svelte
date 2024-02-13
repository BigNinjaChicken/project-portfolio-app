<script lang="ts">
	import '../app.postcss';
	import '../app.css';
	import { onMount, onDestroy } from 'svelte';

	let mobileMenuOpen = false; // Initialize menu state

	// Function to toggle the mobile menu
	function toggleMobileMenu() {
		mobileMenuOpen = !mobileMenuOpen;
	}

	// Close the mobile menu when the component is unmounted
	onDestroy(() => {
		mobileMenuOpen = false;
	});
</script>

<nav class="bg-gray-800 fixed top-0 w-full z-50">
	<div class="mx-auto max-w-7xl px-2 sm:px-6 lg:px-8">
		<div class="relative flex h-16 items-center justify-between">
			<div class="absolute inset-y-0 left-0 flex items-center sm:hidden">
				<!-- Mobile menu button with click event -->
				<button
					type="button"
					class="relative inline-flex items-center justify-center rounded-md p-2 text-gray-400 hover:bg-gray-700 hover:text-white focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white"
					aria-controls="mobile-menu"
					aria-expanded={mobileMenuOpen}
					on:click={toggleMobileMenu}
				>
					<span class="absolute -inset-0.5" />
					<span class="sr-only">Open main menu</span>
					<svg
						class="block h-6 w-6"
						fill="none"
						viewBox="0 0 24 24"
						stroke-width="1.5"
						stroke="currentColor"
						aria-hidden="true"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
						/>
					</svg>
				</button>
			</div>
			<div class="flex flex-1 items-center justify-center sm:items-stretch sm:justify-start">
				<a href="/"
					><div class="flex flex-shrink-0 items-center">
						<img
							class="h-8 w-autotransition-all duration-300 cursor-pointer filter grayscale hover:grayscale-0"
							src="/frazier-logo-purple.png"
							alt="Frazier Kyle"
						/>
					</div></a
				>
				<div class="hidden sm:ml-4 sm:block">
					<div class="flex space-x-4">
						<!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
						<a
							href="/"
							class="text-gray-300 hover:bg-gray-700 hover:text-white rounded-md px-3 py-2 text-sm font-medium"
							>Dashboard</a
						>
						<a
							href="/#recent-projects"
							class="text-gray-300 hover:bg-gray-700 hover:text-white rounded-md px-3 py-2 text-sm font-medium"
							>Featured Projects</a
						>
						<a
							href="/#about-me"
							class="text-gray-300 hover:bg-gray-700 hover:text-white rounded-md px-3 py-2 text-sm font-medium"
							>About Me</a
						>
						<a
							href="/contacts"
							class="text-gray-300 hover:bg-gray-700 hover:text-white rounded-md px-3 py-2 text-sm font-medium"
							>Contacts / Resume</a
						>
					</div>
				</div>
			</div>
			<div class="hidden sm:ml-4 sm:block">
				<div
					class="absolute inset-y-0 right-0 flex items-center pr-2 sm:static sm:inset-auto sm:ml-6 sm:pr-0"
				>
					<a
						href="/portfolio"
						class="inline-flex items-center justify-center p-3 text-base font-medium text-gray-500 rounded-lg bg-gray-50 hover:text-gray-900 hover:bg-gray-100 dark:text-gray-400 dark:bg-gray-800 dark:hover:bg-gray-700 dark:hover:text-white"
					>
						<span class="w-full">🚀 All Programming Projects</span>
						<svg
							class="w-2 h-2 ml-1"
							aria-hidden="true"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 14 10"
						>
							<path
								stroke="currentColor"
								stroke-linecap="round"
								stroke-linejoin="round"
								stroke-width="2"
								d="M1 5h12m0 0L9 1m4 4L9 9"
							/>
						</svg>
					</a>
				</div>
			</div>
		</div>
	</div>

	<!-- Mobile menu, show/hide based on menu state. -->
	<div class="{mobileMenuOpen ? 'block' : 'hidden'} sm:hidden" id="mobile-menu">
		<div class="space-y-1 px-2 pb-3 pt-2">
			<!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
			<a
				on:click={toggleMobileMenu}
				href="/"
				class="text-gray-300 hover:bg-gray-700 hover:text-white block rounded-md px-3 py-2 text-base font-medium"
				>Dashboard</a
			>
			<a
				on:click={toggleMobileMenu}
				href="/#recent-projects"
				class="text-gray-300 hover:bg-gray-700 hover:text-white block rounded-md px-3 py-2 text-base font-medium"
				>Featured Projects</a
			>
			<a
				on:click={toggleMobileMenu}
				href="/#about-me"
				class="text-gray-300 hover:bg-gray-700 hover:text-white block rounded-md px-3 py-2 text-base font-medium"
				>About Me</a
			>
			<a
				on:click={toggleMobileMenu}
				href="/contacts"
				class="text-gray-300 hover:bg-gray-700 hover:text-white block rounded-md px-3 py-2 text-base font-medium"
				>Contacts / Resume</a
			>
			<a
				on:click={toggleMobileMenu}
				href="/portfolio"
				class="text-gray-300 hover:bg-gray-700 hover:text-white block rounded-md px-3 py-2 text-base font-medium"
			>
				<span class="w-full">🚀 My Programming Projects</span>
			</a>
		</div>
	</div>
</nav>

<slot />

<footer class="bg-white rounded-lg shadow m-4 dark:bg-gray-800">
	<div class="w-full mx-auto max-w-screen-xl p-4 md:flex md:items-center md:justify-between">
		<span class="text-sm text-gray-500 sm:text-center dark:text-gray-400"
			>2023 <a href="https://flowbite.com/" class="hover:underline">Frazier Kyle's Portfolio</a>.
			All Rights Reserved.
		</span>
		<ul
			class="flex flex-wrap items-center mt-3 text-sm font-medium text-gray-500 dark:text-gray-400 sm:mt-0"
		>
			<li>
				<a href="/contacts" class="mr-4 hover:underline md:mr-6">Contacts / Resume</a>
			</li>
			<li>
				<a href="https://www.linkedin.com/in/frazierkyle/" class="mr-4 hover:underline md:mr-6"
					>LinkedIn</a
				>
			</li>
			<li>
				<a
					href="https://github.com/BigNinjaChicken/project-portfolio-app"
					class="mr-4 hover:underline md:mr-6">GitHub Portfolio Repo</a
				>
			</li>
			<li>
				<a
					href="https://github.com/BigNinjaChicken/project-portfolio-app/blob/main/LICENSE"
					class="hover:underline">License</a
				>
			</li>
		</ul>
	</div>
</footer>
