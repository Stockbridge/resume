<script lang="ts">
	import SectionHeader from '$lib/SectionHeader.svelte';
	export let skills: string[][];
</script>

<section class="mb-6">
	<SectionHeader text="Skills" />
	<ul class="flex">
		{#each skills as skillRow}
			{#each skillRow as skill}
				<li>{skill}</li>
			{/each}
		{/each}
	</ul>
</section>
