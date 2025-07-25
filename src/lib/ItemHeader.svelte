<script lang="ts">
  export let title: string;
  export let dates: string | undefined;
  export let subtitle: string | undefined;
  export let location: string | undefined;
</script>

<div class="flex flex-col text-gray-400 text-sm mb-2">
    <div class="flex flex-row justify-between border-b border-gray-200">
        <h3 class="font-semibold text-base text-gray-800">{title}</h3>
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
