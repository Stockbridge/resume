<script lang="ts">
  export let firstName: string;
  export let lastName: string;
  export let email: string;
  export let phone: string;
</script>

<header class="mb-8 relative flex pr-2">
    <h1 class="text-4xl font-extrabold tracking-tighter text-gray-900 lowercase flex flex-col leading-none pl-4 absolute ">
        <span class="absolute text-6xl font-medium left-0 -top-1 text-blue-500 bg-white z-0">{'\{'}</span>
      <span class="z-1">{firstName}</span>
      <span class="pl-3 pr-2 -mt-3 bg-white">{lastName}</span>
    </h1>
    <div class="flex flex-col flex-grow-1 items-end text-gray-500 flex-shrink-0 justify-self-start border-b border-blue-300 tracking-tight">
      <span class="text-l font-medium text-gray-700">{email}</span>
      <span class="text-base text-s">{phone}</span>
    </div>
</header>
