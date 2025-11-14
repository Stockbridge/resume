<script lang="ts">
	import SectionHeader from '$lib/SectionHeader.svelte';
	import ItemHeader from '$lib/ItemHeader.svelte';
	export let education: {
		degree: string;
		school: string;
		dates: string;
		description?: string;
	};
</script>

<section class="mb-8">
	<SectionHeader text="educationcation" />
	<div class="mb-4">
		<ItemHeader
			title={education.degree}
			dates={education.dates}
			subtitle={education.school}
			location={undefined}
		/>
		{#if education.description}
			<div class="mt-1 text-sm text-gray-600">{education.description}</div>
		{/if}
	</div>
</section>
