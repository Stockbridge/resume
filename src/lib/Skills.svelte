<script lang="ts">
  export let skills: string[][];
</script>

<section class="mb-8">
  <h2 class="text-xl font-bold text-blue-900 border-b border-blue-200 pb-1 mb-3 tracking-wide uppercase">Skills</h2>
  <ul class="grid grid-cols-2 gap-x-6 gap-y-1 text-gray-700 text-base ml-2">
    {#each skills as skillRow}
      {#each skillRow as skill}
        <li>{skill}</li>
      {/each}
    {/each}
  </ul>
</section>
