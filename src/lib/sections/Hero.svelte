<script>
	import WaMessage from '$lib/components/WaMessage.svelte';
	import recommendations from '$lib/recommendations.json';
	import ContactButtons from '$lib/components/ContactButtons.svelte';
	import RecommendationsPanel from '$lib/components/RecommendationsPanel.svelte';
</script>

<section>
	<main class="relative -mt-16 h-screen rounded-t-3xl bg-linear-to-br from-white via-blue-50 to-indigo-50 shadow-2xl">
		<article class="relative flex h-full flex-col justify-between gap-2 px-2 md:flex-row-reverse">
			<header class="mt-3 self-center px-4">
				<hgroup class="mt-7 text-center">
					<h1
						class="mb-5 bg-linear-to-r from-blue-600 to-indigo-600 bg-clip-text text-4xl font-extrabold tracking-tight text-transparent drop-shadow-sm md:text-5xl"
					>
						מורה אישי להצלחה
					</h1>
					<p class="mx-auto max-w-xl text-center text-lg font-normal leading-relaxed tracking-wide text-slate-700">
						אחרי מאות תלמידים ועשור של ניסיון, אני יכול להגיד בבטחון שאני יודע ללמד כל תלמיד איך
						להצליח במבחנים ובכיתה. <span class="font-semibold text-blue-600">כל תלמיד יכול להצליח</span>
					</p>
				</hgroup>
				<ContactButtons />
			</header>
			<RecommendationsPanel {recommendations} />
		</article>
	</main>
</section>
