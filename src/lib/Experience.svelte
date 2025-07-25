<script lang="ts">
	import SectionHeader from '$lib/SectionHeader.svelte';
	export let experience: Array<{
		role: string;
		company: string;
		dates: string;
		bullets: string[];
	}>;
</script>

<section class="mb-8">
	<SectionHeader text="Experience" />
	{#each experience as job}
		<div class="mb-6">
			<div class="flex flex-col sm:flex-row sm:items-center sm:justify-between">
				<h3 class="text-lg font-semibold text-gray-800">
					{job.role} <span class="font-normal text-gray-500">– {job.company}</span>
				</h3>
				<span class="mt-1 text-sm text-gray-400 sm:mt-0">{job.dates}</span>
			</div>
			<ul class="mt-2 ml-6 list-disc space-y-1 text-gray-700">
				{#each job.bullets as bullet}
					<li>{bullet}</li>
				{/each}
			</ul>
		</div>
	{/each}
</section>
