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
	<div class="py-8">
		<div class="container mx-auto text-center drop-shadow-lg">
			<div class="bg-surface-600 bg-opacity-50 rounded-lg inline-block p-4">
				<h1 class="h1">
					<span
						class="bg-gradient-to-br from-pink-500 to-violet-500 bg-clip-text text-transparent box-decoration-clone"
						>Contacts.</span
					>
				</h1>
				<div class="mt-4 text-secondary-100">
					<div class="rounded-lg mx-20">
						<!-- Add this div for the small box -->
						<p>Feel free to contact me if you want</p>
                        <p>to discuss any of my projects.</p>
					</div>
				</div>
				<div class="mt-8">
					<p class="text-lg">Frazier E. Kyle 👋</p>
					<p class="text-lg">
						<a href="tel:(513)-882-6736" class="text-blue-300 hover:underline">(513)-882-6736 📞</a>
					</p>
					<p class="text-lg">
						<a href="mailto:frazierkyle1235@gmail.com" class="text-blue-300 hover:underline"
							>frazierkyle1235@gmail.com 📨</a
						>
					</p>
					<p class="text-lg">
						<a href="https://github.com/BigNinjaChicken/project-portfolio-app" class="text-blue-300 hover:underline"
							>GitHub Link 💾</a
						>
					</p>
                    <p class="text-lg">
						<a href="https://www.linkedin.com/in/frazierkyle/" class="text-blue-300 hover:underline target:shadow-lg"
							>LinkedIn 🔗</a
						>
					</p>
				</div>
			</div>
		</div>
	</div>

	<div class="py-4">
		<div class="container mx-auto text-center drop-shadow-lg">
			<a href={Resume} target="_blank" type="button" class="btn variant-filled drop-shadow-lg">
				<p class="mx-10 p-3 text-2xl">Resume</p>
            </a>

			<div class="mt-4">
				<svelte:component this={PdfViewer} url={Resume} />
			</div>
		</div>
	</div>
</main>
