<script lang="ts">
	import Book from '$lib/portfolio/progress-book.pdf';
	import { onMount } from 'svelte';

	let PdfViewer: any;
	onMount(async () => {
		const module = await import('svelte-pdf');
		PdfViewer = module.default;
	});
</script>

<main class="pt-16">
	<div class="container mx-auto p-10 pb-2">
		<h1 class="text-white text-5xl tracking-small text-center" id="recent-projects">
			<span
				class="bg-gradient-to-br from-blue-500 to-cyan-300 bg-clip-text text-transparent box-decoration-clone"
				>XR Progress Book</span
			>
		</h1>
		<h2 class="text-surface-400 text-2xl tracking-small text-center pt-2" id="recent-projects">
			List of projects my team created for our senior design project at Miami University
		</h2>
	</div>

	<div class="py-4">
        <div class="container mx-auto text-center drop-shadow-lg">
            <a href={Book} target="_blank" type="button" class="btn variant-filled drop-shadow-lg">
                <p class="mx-10 p-3 text-2xl">2024 Miami Univerity Project Book</p>
            </a>
    
            <!-- Hide PDF viewer on small screens (e.g., screens smaller than md) -->
            <div class="mt-4 hidden md:block">
                <svelte:component this={PdfViewer} url={Book} />
            </div>
        </div>
    </div>
</main>