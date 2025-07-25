<script lang="ts">
  import SectionHeader from '$lib/SectionHeader.svelte';
  import ItemHeader from '$lib/ItemHeader.svelte';
  export let projects: Array<{
    title: string;
    dates?: string;
    context?: string;
    bullets: string[];
  }>;
</script>

<section class="mb-8">
  <SectionHeader text="Projects" />
  {#each projects as project}
    <div class="mb-6">
      <ItemHeader title={project.title} dates={project.dates} subtitle={project.context} location={undefined}/>
      <ul class="list-disc ml-6 mt-2 text-gray-700 space-y-1">
        {#each project.bullets as bullet}
          <li>{bullet}</li>
        {/each}
      </ul>
    </div>
  {/each}
</section>
