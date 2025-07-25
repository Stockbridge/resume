<script lang="ts">
	import SectionHeader from '$lib/SectionHeader.svelte';
	import ItemHeader from '$lib/ItemHeader.svelte';
	export let education: Array<{
		degree: string;
		school: string;
		dates: string;
		description?: string;
	}>;
</script>

<section class="mb-8">
	<SectionHeader text="Education" />
	{#each education as edu}
		<div class="mb-4">
			<ItemHeader title={edu.degree} dates={edu.dates} subtitle={edu.school} location={undefined} />
			{#if edu.description}
				<div class="mt-1 text-sm text-gray-600">{edu.description}</div>
			{/if}
		</div>
	{/each}
</section>
