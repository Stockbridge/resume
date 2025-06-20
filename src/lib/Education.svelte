<script lang="ts">
  export let education: Array<{
    degree: string;
    school: string;
    dates: string;
    description?: string;
  }>;
</script>

<section class="mb-8">
  <h2 class="text-xl font-bold text-blue-900 border-b border-blue-200 pb-1 mb-3 tracking-wide uppercase">Education</h2>
  {#each education as edu}
    <div class="mb-4">
      <div class="flex flex-col sm:flex-row sm:justify-between sm:items-center">
        <h3 class="font-semibold text-lg text-gray-800">{edu.degree}</h3>
        <span class="text-sm text-gray-400 mt-1 sm:mt-0">{edu.school} – {edu.dates}</span>
      </div>
      {#if edu.description}
        <div class="text-gray-600 text-sm mt-1">{edu.description}</div>
      {/if}
    </div>
  {/each}
</section>
