<script>
	import Hero from '$lib/sections/Hero.svelte';
	import About from '$lib/sections/About.svelte';
	import Services from '$lib/sections/Services.svelte';
</script>

<div class="h-20 bg-black"></div>

<Hero />

<About />

<Services />

<!-- מחירים -->
<section class="bg-white">
	<!-- <div class="mx-auto max-w-7xl px-6 lg:px-8">
		<div class="mx-auto max-w-2xl lg:max-w-none">
			<div>
				<h1>
					<span class="block font-display text-base font-semibold text-neutral-950">
						תעריפים
					</span>
					<span class="sr-only">-</span>
					<span class="mt-6 block max-w-5xl font-display text-5xl font-medium tracking-tight text-balance text-neutral-950 sm:text-6xl">
						שיעור פרטי
					</span>
				</h1>
			</div>
		</div>
	</div> -->

	<!-- Pricing Card -->
	<div class="mx-auto max-w-md px-6 lg:px-8">
		<div class="rounded-3xl border border-neutral-200 bg-white p-8 shadow-sm">
			<div class="text-center">
				<div class="mb-6">
					<div
						class="mb-6 inline-block rounded-full bg-gradient-to-r from-purple-600 to-purple-700 px-5 py-2 text-base font-medium text-white"
					>
						מחיר שקוף וקבוע
					</div>
					<div>
						<span class="text-6xl font-bold tracking-tight text-neutral-950">125</span>
						<span class="text-2xl font-medium text-neutral-600">₪</span>
					</div>
					<div class="mt-3 text-base text-neutral-600">לשיעור של 45 דקות</div>
				</div>
				<div class="space-y-3 text-right">
					<div class="flex items-center gap-3">
						<div class="flex h-5 w-5 items-center justify-center rounded-full bg-neutral-100">
							<div class="h-2 w-2 rounded-full bg-neutral-600"></div>
						</div>
						<div class="flex-1 text-sm text-neutral-700">התשלום מתבצע בתום השיעור</div>
					</div>
					<div class="flex items-center gap-3">
						<div class="flex h-5 w-5 items-center justify-center rounded-full bg-neutral-100">
							<div class="h-2 w-2 rounded-full bg-neutral-600"></div>
						</div>
						<div class="flex-1 text-sm text-neutral-700">
							ביטול שיעור מחייב הודעה מראש של 12 שעות לפחות
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- אזורי השירות -->
<section class="bg-neutral-100 px-6 py-16">
	<div class="mx-auto max-w-4xl">
		<h2 class="font-display mb-8 text-4xl font-semibold tracking-wider text-neutral-950">
			אזורי השירות
		</h2>
		<div class="space-y-6 text-neutral-700">
			<p class="mb-6 text-xl">אני מגיע לבית התלמיד באזורים הבאים:</p>
			<ul class="grid grid-cols-2 gap-4 text-lg md:grid-cols-4">
				<li class="rounded-2xl bg-white p-4 text-center font-medium text-neutral-950">
					פתח תקווה
				</li>
				<li class="rounded-2xl bg-white p-4 text-center font-medium text-neutral-950">רמת גן</li>
				<li class="rounded-2xl bg-white p-4 text-center font-medium text-neutral-950">גבעתיים</li>
				<li class="rounded-2xl bg-white p-4 text-center font-medium text-neutral-950">
					קריית אונו
				</li>
			</ul>
			<p class="mt-8 text-xl font-semibold text-neutral-950">שיעורים מקוונים זמינים לכל הארץ</p>
		</div>
	</div>
</section>

<!-- שאלות נפוצות -->
<section class="bg-neutral-950 px-6 py-16">
	<div class="mx-auto max-w-4xl">
		<h2 class="font-display mb-12 text-4xl font-semibold tracking-wider text-neutral-50">
			שאלות נפוצות
		</h2>

		<div class="space-y-8">
			<div class="border-s-4 border-neutral-700 ps-6">
				<h3 class="font-display mb-3 text-xl font-semibold text-neutral-200">
					כמה זמן לוקח לראות שיפור בציונים?
				</h3>
				<p class="leading-relaxed text-neutral-400">
					בדרך כלל תלמידים רואים שיפור ניכר כבר אחרי 3-4 שיעורים. השיפור תלוי ברמת התלמיד ובהשקעה
					שלו בבית.
				</p>
			</div>

			<div class="border-s-4 border-neutral-700 ps-6">
				<h3 class="font-display mb-3 text-xl font-semibold text-neutral-200">
					האם אתה מספק חומרי לימוד?
				</h3>
				<p class="leading-relaxed text-neutral-400">
					כן, אני מכין חומרי לימוד מותאמים, תרגילים נוספים וסיכומי חומר לפי הצורך של כל תלמיד.
				</p>
			</div>

			<div class="border-s-4 border-neutral-700 ps-6">
				<h3 class="font-display mb-3 text-xl font-semibold text-neutral-200">
					מה קורה אם התלמיד לא מבין משהו בשיעור?
				</h3>
				<p class="leading-relaxed text-neutral-400">
					אני תמיד זמין לשאלות גם בין השיעורים דרך הודעות או טלפון. החזרה על החומר היא חלק בלתי
					נפרד מהתהליך.
				</p>
			</div>

			<div class="border-s-4 border-neutral-700 ps-6">
				<h3 class="font-display mb-3 text-xl font-semibold text-neutral-200">
					מה המלצת לגבי תדירות השיעורים?
				</h3>
				<p class="leading-relaxed text-neutral-400">
					בדרך כלל אני ממליץ על שיעור אחד בשבוע לתלמידים רגילים, ושני שיעורים בשבוע לתלמידים
					שצריכים שיפור מהיר או לקראת בחינות.
				</p>
			</div>
		</div>
	</div>
</section>

<!-- איפה אני מלמד -->
<section class="bg-neutral-50 px-6 py-20">
	<div class="mx-auto max-w-4xl text-center">
		<h2 class="font-display mb-12 text-5xl font-extrabold tracking-wider text-neutral-950">
			איפה אני מלמד?
		</h2>
		<p class="mx-auto max-w-3xl text-justify text-xl leading-relaxed text-neutral-700">
			אני מלמד פרונטלית באזורים רמת גן, גבעתיים, פתח תקווה וקריית אונו, מתוך אמונה שהשיעור
			הפרונטלי הוא הדרך האפקטיבית ביותר ללמידה. בנוסף, אני מציע גם שיעורים מרוחקים דרך המחשב, כך
			שאני יכול לעזור לכם מכל מקום בארץ. עם זאת, אם באזור שלכם יש מורה פרונטלי טוב, אני ממליץ בחום
			לבחור באפשרות הזו – איכות השיעור במפגש פנים אל פנים תמיד תהיה גבוהה יותר. בין אם פרונטלית
			ובין אם מרחוק, אני כאן כדי לעזור לכם להצליח!
		</p>
	</div>
</section>
