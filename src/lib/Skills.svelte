<script lang="ts">
	import SectionHeader from '$lib/SectionHeader.svelte';
	export let skills: { title: string; items: string[] }[];
</script>

<div class="mb-6 flex flex-col gap-6 sm:flex-row sm:flex-wrap">
	{#each skills as skill}
		<section class="mb-2 flex shrink-0 flex-grow flex-col sm:w-1/3">
			<SectionHeader text={skill.title} />
			<ul class="">
				{#each skill.items as item}
					<li>{item}</li>
				{/each}
			</ul>
		</section>
	{/each}
</div>
