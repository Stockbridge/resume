<script lang="ts">
  export let employment: Array<{
    company: string;
    dates: string;
    title: string;
    website?: string;
    description?: string;
    skills?: string;
  }>;
</script>

<section class="mb-8">
  <h2 class="text-xl font-bold text-blue-900 border-b border-blue-200 pb-1 mb-3 tracking-wide uppercase">Employment</h2>
  {#each employment as job}
    <div class="mb-6">
      <div class="flex flex-col sm:flex-row sm:justify-between sm:items-center">
        <h3 class="font-semibold text-lg text-gray-800">{job.company}{#if job.website} <a href={job.website} class="text-blue-600 underline text-base font-normal ml-2">{job.website.replace('https://','').replace('http://','')}</a>{/if}</h3>
        <span class="text-sm text-gray-400 mt-1 sm:mt-0">{job.dates}</span>
      </div>
      <div class="text-gray-700 font-medium">{job.title}</div>
      {#if job.description}
        <div class="text-gray-600 text-sm mt-1">{job.description}</div>
      {/if}
      {#if job.skills}
        <div class="text-gray-500 text-xs mt-1">{job.skills}</div>
      {/if}
    </div>
  {/each}
</section>
