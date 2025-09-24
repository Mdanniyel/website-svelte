<script>
	import RecommendationColumn from '$lib/components/RecommendationColumn.svelte';

	let { recommendations } = $props();
</script>

<aside class="relative my-4 flex gap-2 overflow-hidden">
	<RecommendationColumn recommendations={recommendations.slice(0)} additionalClasses="" />
	<RecommendationColumn
		recommendations={recommendations.slice(4)}
		additionalClasses="lg:block hidden"
	/>
	<RecommendationColumn
		recommendations={recommendations.slice(2)}
		additionalClasses="xl:block hidden"
	/>

	<div class="pointer-events-none absolute inset-x-0 top-0 h-32 bg-linear-to-b from-white"></div>
	<!-- <div class="pointer-events-none absolute inset-x-0 top-0 h-32 bg-linear-to-r from-cyan-500 to-blue-500"></div> -->
	<div class="pointer-events-none absolute inset-x-0 bottom-0 h-32 bg-linear-to-t from-white"></div>
</aside>
