<script>
	import Feature from '$lib/components/Feature.svelte';
</script>

<section class="bg-black py-12 sm:py-16 lg:py-20">
	<div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
		<div class="text-center">
			<h2 class="text-3xl leading-tight font-bold text-white sm:text-4xl xl:text-5xl">
				UiBun helps you build stunning websites
			</h2>
			<p class="mt-4 text-base leading-7 text-neutral-300 sm:mt-8">
				Lorem ipsum dolor sit amet, consectetur adipis elit
			</p>
		</div>

		<div
			class="mt-10 grid grid-cols-1 gap-y-12 text-center sm:mt-16 sm:grid-cols-2 sm:gap-x-12 md:grid-cols-3 md:gap-px md:bg-slate-900 xl:mt-24"
		>
			<Feature />
			<Feature />
			<Feature />
			<Feature />
			<Feature />
			<Feature />
		</div>
	</div>
</section>
