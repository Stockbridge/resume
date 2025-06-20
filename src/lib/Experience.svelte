<script lang="ts">
  export let experience: Array<{
    role: string;
    company: string;
    dates: string;
    bullets: string[];
  }>;
</script>

<section class="mb-8">
  <h2 class="text-xl font-bold text-blue-900 border-b border-blue-200 pb-1 mb-3 tracking-wide uppercase">Experience</h2>
  {#each experience as job}
    <div class="mb-6">
      <div class="flex flex-col sm:flex-row sm:justify-between sm:items-center">
        <h3 class="font-semibold text-lg text-gray-800">{job.role} <span class="text-gray-500 font-normal">– {job.company}</span></h3>
        <span class="text-sm text-gray-400 mt-1 sm:mt-0">{job.dates}</span>
      </div>
      <ul class="list-disc ml-6 mt-2 text-gray-700 space-y-1">
        {#each job.bullets as bullet}
          <li>{bullet}</li>
        {/each}
      </ul>
    </div>
  {/each}
</section>
