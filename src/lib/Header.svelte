<script lang="ts">
	export let firstName: string;
	export let lastName: string;
	export let email: string;
	export let phone: string;
</script>

<header class="relative mb-8 flex pr-2">
	<h1
		class="absolute flex flex-col pl-4 text-4xl leading-none font-extrabold tracking-tighter text-gray-900 lowercase"
	>
		<span class="absolute -top-1 left-0 z-0 bg-white text-6xl font-medium text-blue-500"
			>{'\{'}</span
		>
		<span class="z-1">{firstName}</span>
		<span class="-mt-3 bg-white pr-2 pl-3">{lastName}</span>
	</h1>
	<div
		class="flex flex-shrink-0 flex-grow-1 flex-col items-end justify-self-start border-b border-blue-300 tracking-tight text-gray-500"
	>
		<span class="text-l font-medium text-gray-700">{email}</span>
		<span class="text-s text-base">{phone}</span>
	</div>
</header>
