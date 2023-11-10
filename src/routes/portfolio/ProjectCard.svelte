<!-- ProjectCard.svelte -->

<script lang="ts">
	// Define a prop for the project data
	export let project: any;
</script>

<a href={project.href || './contacts'} class="card card-hover shadow-lg my-auto">
	<img class="w-full rounded-t-lg" src={project.image} alt={project.title} />

	<div class="px-6 py-4 text-left">
		<h1 class="font-bold text-4xl mb-2 text-primary-500 italic ">{project.title}</h1>
		<h2 class="text-secondary-400">{project.role}</h2>
		<p class="mt-4">{project.description}</p>
		<div class="flex justify-between items-center mt-3">
			<p class="text-surface-400 text-sm">{project.date}</p>
			<p class="text-right text-surface-400 text-sm">{project.location}</p>
		</div>
	</div>
</a>
