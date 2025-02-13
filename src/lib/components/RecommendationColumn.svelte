<script>
	import WaMessage from '$lib/components/WaMessage.svelte';

	let { recommendations, additionalClasses } = $props();
</script>

<section class="{additionalClasses} min-w-64 grow overflow-hidden">
	<ul class="slide-top space-y-5">
		{#each recommendations as recommendation}
			<li>
				<WaMessage text={recommendation} />
			</li>
		{/each}
		{#each recommendations as recommendation}
			<li>
				<WaMessage text={recommendation} />
			</li>
		{/each}
	</ul>
</section>

<style>
	ul.slide-top {
		animation: slide-top 70s linear infinite both;
	}

	@keyframes slide-top {
		100% {
			transform: translateY(-50%);
		}
	}
</style>
