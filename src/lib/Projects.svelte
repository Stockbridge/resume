<script lang="ts">
  export let projects: Array<{
    title: string;
    dates?: string;
    context?: string;
    bullets: string[];
  }>;
</script>

<section class="mb-8">
  <h2 class="text-xl font-bold text-blue-900 border-b border-blue-200 pb-1 mb-3 tracking-wide uppercase">Projects</h2>
  {#each projects as project}
    <div class="mb-6">
      <div class="flex flex-col sm:flex-row sm:justify-between sm:items-center">
        <h3 class="font-semibold text-lg text-gray-800">{project.title}</h3>
        {#if project.dates}
          <span class="text-sm text-gray-400 mt-1 sm:mt-0">{project.dates}</span>
        {/if}
      </div>
      {#if project.context}
        <div class="text-sm text-gray-500 mb-1">{project.context}</div>
      {/if}
      <ul class="list-disc ml-6 mt-2 text-gray-700 space-y-1">
        {#each project.bullets as bullet}
          <li>{bullet}</li>
        {/each}
      </ul>
    </div>
  {/each}
</section>
