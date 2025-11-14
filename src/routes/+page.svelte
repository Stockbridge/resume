<script lang="ts">
	import Header from '$lib/Header.svelte';
	import Education from '$lib/Education.svelte';
	import Skills from '$lib/Skills.svelte';
	import Projects from '$lib/Projects.svelte';
	import Employment from '$lib/Employment.svelte';
	
	import header from '$lib/data/header.json';
	import education from '$lib/data/education.json';
	import skills from '$lib/data/skills.json';
	import projects from '$lib/data/projects.json';
	import employment from '$lib/data/employment.json';
</script>

<main class="mx-auto max-w-210">
	<Header {...header} />
	<div class="pr-2 pl-6">
		<Skills {skills} />

		<div class="flex flex-col gap-6 sm:flex-row">
			<div class="flex-1 sm:w-1/2">
				<Employment {employment} />
			</div>
			<div class="flex-1 sm:w-1/2">
				<Education {education} />
				<Projects {projects} />
			</div>
		</div>
	</div>
</main>
