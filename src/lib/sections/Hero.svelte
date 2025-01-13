<script>
	import WaMessage from "./WaMessage.svelte";
	import recommendations from "$lib/recommendations.json";
</script>

<section>
	<div class="relative -mt-16 h-screen rounded-t-3xl bg-white">
		<div class="relative flex h-full flex-col justify-between space-x-1.5 md:flex-row-reverse">
			<!-- text and bottens -->
			<div class="mx-2.5 mt-3 self-center">
				<div class="mt-7 text-center">
					<h1
						class="mb-5 bg-gradient-to-r from-stone-900 to-stone-700 bg-clip-text text-3xl font-bold tracking-wider text-transparent"
					>
						מורה אישי להצלחה
					</h1>
					<p class="text-center text-lg font-light tracking-wide">
						אחרי מאות תלמידים ועשור של ניסיון, אני יכול להגיד בבטחון שאני יודע ללמד כל תלמיד איך
						להצליח במבחנים ובכיתה. כל תלמיד יכול להצליח
					</p>
				</div>
				<div class="mt-4 flex justify-center gap-3.5 text-center text-3xl">
					<button
						type="button"
						class="grow rounded-lg border border-black bg-gradient-to-r from-stone-900 to-stone-800 py-1.5 text-white hover:bg-gradient-to-br focus:ring-4 focus:ring-blue-300 dark:focus:ring-blue-800"
					>
						<i class="fa fa-phone"></i>
					</button>
					<button
						type="button"
						class="grow rounded-lg border border-black py-1.5 hover:bg-gradient-to-br focus:ring-4 focus:ring-green-300 dark:focus:ring-green-800"
					>
						<i class="fa fa-whatsapp"></i>
					</button>
				</div>
			</div>
			<div class="relative my-4 flex overflow-hidden">
				
				<div class="grow overflow-hidden px-3 min-w-64">
					<div class="slide-top">
						{#each recommendations.slice(0) as recommendation}
							<WaMessage text={recommendation}/>
						{/each}
					</div>
				</div>
				
				<div class="hidden grow overflow-hidden px-3 min-w-64 lg:block">
					<div class="slide-top">
						{#each recommendations.slice(4) as recommendation}
							<WaMessage text={recommendation}/>
						{/each}
					</div>
				</div>
				
				<div class="hidden grow overflow-hidden px-3 min-w-64 xl:block">
					<div class="slide-top">
						{#each recommendations.slice(2) as recommendation}
							<WaMessage text={recommendation}/>
						{/each}
					</div>
				</div>

				<div
					class="pointer-events-none absolute inset-x-0 top-0 h-32 bg-gradient-to-b from-white"
				></div>
				<div
					class="pointer-events-none absolute inset-x-0 bottom-0 h-32 bg-gradient-to-t from-white"
				></div>
			</div>
		</div>
	</div>
</section>

<style>
	.slide-top {
		animation: slide-top 140s linear infinite both;
	}

	@keyframes slide-top {
		100% {
			transform: translateY(-50%);
		}
	}
</style>
