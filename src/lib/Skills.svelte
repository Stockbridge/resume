<script lang="ts">
	import SectionHeader from '$lib/SectionHeader.svelte';
	export let skills: { title: string; items: string[] }[];
</script>

{#each skills as skill}
	<section class="mb-6">
		<SectionHeader text={skill.title} />
		<ul class="flex">
			{#each skill.items as skillRow}
				{#each skillRow as skill}
					<li>{skill}</li>
				{/each}
			{/each}
		</ul>
	</section>
{/each}
