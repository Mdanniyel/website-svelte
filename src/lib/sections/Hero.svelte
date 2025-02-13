<script>
	import WaMessage from '$lib/components/WaMessage.svelte';
	import recommendations from '$lib/recommendations.json';
	import ContactButtons from '$lib/components/ContactButtons.svelte';
	import RecommendationsPanel from '$lib/components/RecommendationsPanel.svelte';
</script>

<section>
	<main class="relative -mt-16 h-screen rounded-t-3xl bg-white">
		<article class="relative flex h-full flex-col justify-between gap-2 px-2 md:flex-row-reverse">
			<header class="mt-3 self-center">
				<hgroup class="mt-7 text-center">
					<h1
						class="mb-5 bg-gradient-to-r from-stone-900 to-stone-700 bg-clip-text text-3xl font-bold tracking-wider text-transparent"
					>
						מורה אישי להצלחה
					</h1>
					<p class="text-center text-lg font-light tracking-wide">
						אחרי מאות תלמידים ועשור של ניסיון, אני יכול להגיד בבטחון שאני יודע ללמד כל תלמיד איך
						להצליח במבחנים ובכיתה. כל תלמיד יכול להצליח
					</p>
				</hgroup>
				<ContactButtons />
			</header>
			<RecommendationsPanel {recommendations} />
		</article>
	</main>
</section>
