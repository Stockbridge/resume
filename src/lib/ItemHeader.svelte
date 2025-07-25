<script lang="ts">
	export let title: string;
	export let dates: string | undefined;
	export let subtitle: string | undefined;
	export let location: string | undefined;
</script>

<div class="mb-2 flex flex-col text-sm text-gray-400">
	<div class="flex flex-row justify-between border-b border-gray-200">
		<h3 class="text-base font-semibold text-gray-800">{title}</h3>
		{#if dates}
			<span class="text-sm">{dates}</span>
		{/if}
	</div>
	<div class="flex flex-row justify-between">
		{#if subtitle}
			<span>{subtitle}</span>
		{/if}
		{#if location}
			<span>{location}</span>
		{/if}
	</div>
</div>
