<script lang="ts">
	import Resume from '$lib/contacts/resume.pdf';
	import { onMount } from 'svelte';

	let PdfViewer: any;
	onMount(async () => {
		const module = await import('svelte-pdf');
		PdfViewer = module.default;
	});
</script>

<main class="pt-16">
	<div class="bg-gray-200 py-8">
		<div class="container mx-auto text-center">
			<h2 class="text-3xl font-semibold text-gray-800">Contacts</h2>
			<p class="mt-4 text-gray-600">
				Feel free to contact me if you want to discuss any of my projects.
			</p>

			<div class="mt-8">
				<p class="text-lg text-gray-800">Frazier E. Kyle</p>
				<p class="text-lg text-gray-800">
					<a href="tel:(513)-882-6736" class="text-blue-500 hover:underline">(513)-882-6736</a>
				</p>
				<p class="text-lg text-gray-800">
					<a href="mailto:kylefe@miamioh.edu" class="text-blue-500 hover:underline"
						>kylefe@miamioh.edu</a
					>
				</p>
				<p class="text-lg text-gray-800">
					<a href="https://github.com/yourusername" class="text-blue-500 hover:underline"
						>GitHub Link</a
					>
				</p>
			</div>
		</div>
	</div>

	<div class="py-8">
		<div class="container mx-auto text-center">
			<h2 class="text-3xl font-semibold text-gray-800">Resume</h2>

			<div class="mt-8">
				<svelte:component this={PdfViewer} url={Resume} />
			</div>
		</div>
	</div>
</main>
