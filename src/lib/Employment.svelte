<script lang="ts">
	import SectionHeader from '$lib/SectionHeader.svelte';
	import ItemHeader from '$lib/ItemHeader.svelte';
	export let employment: Array<{
		company: string;
		dates: string;
		title: string;
		location?: string;
		website?: string;
		skills?: string[];
	}>;
</script>

<section>
	<SectionHeader text="Employment" />
	{#each employment as job}
		<div class="mb-3">
			<ItemHeader
				title={job.company}
				dates={job.dates}
				subtitle={job.title}
				location={job.location}
			/>
			{#if job.skills}
				{#each job.skills as skill}
					<div class="mt-1 text-xs text-gray-500">{skill}</div>
				{/each}
			{/if}
		</div>
	{/each}
</section>
