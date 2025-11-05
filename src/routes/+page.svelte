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
<section class="bg-white py-24 sm:py-32">
	<div class="mx-auto max-w-7xl px-6 lg:px-8">
		<div class="mx-auto max-w-2xl text-center">
			<h2 class="text-3xl font-bold tracking-tight text-neutral-900 sm:text-4xl">תעריפים</h2>
			<p class="mt-6 text-lg leading-8 text-neutral-600">
				מחירים שקופים וללא הפתעות - להתמקד בלמידה, לא בכסף
			</p>
		</div>

		<!-- Pricing Card -->
		<div class="mx-auto mt-16 max-w-lg">
			<div class="rounded-4xl bg-white p-10 shadow-lg ring-1 ring-neutral-200 transition-all hover:shadow-xl hover:ring-neutral-300">
				<div class="text-center">
					<div class="mb-8">
						<div
							class="mb-8 inline-block rounded-full bg-gradient-to-r from-purple-600 to-purple-700 px-6 py-2.5 text-base font-semibold text-white shadow-lg"
						>
							מחיר שקוף וקבוע
						</div>
						<div class="flex items-baseline justify-center gap-x-2">
							<span class="text-7xl font-bold tracking-tight text-neutral-950">125</span>
							<span class="text-3xl font-semibold text-neutral-600">₪</span>
						</div>
						<div class="mt-4 text-lg font-medium text-neutral-600">לשיעור של 45 דקות</div>
					</div>
					
					<div class="space-y-4 border-t border-neutral-200 pt-8 text-right">
						<div class="flex items-start gap-4">
							<div class="flex h-6 w-6 flex-shrink-0 items-center justify-center rounded-full bg-purple-100">
								<svg class="h-4 w-4 text-purple-600" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2.5">
									<path stroke-linecap="round" stroke-linejoin="round" d="M5 13l4 4L19 7" />
								</svg>
							</div>
							<div class="flex-1 text-base text-neutral-700 leading-relaxed">
								התשלום מתבצע בתום השיעור
							</div>
						</div>
						<div class="flex items-start gap-4">
							<div class="flex h-6 w-6 flex-shrink-0 items-center justify-center rounded-full bg-purple-100">
								<svg class="h-4 w-4 text-purple-600" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2.5">
									<path stroke-linecap="round" stroke-linejoin="round" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
								</svg>
							</div>
							<div class="flex-1 text-base text-neutral-700 leading-relaxed">
								ביטול שיעור מחייב הודעה מראש של 12 שעות לפחות
							</div>
						</div>
						<div class="flex items-start gap-4">
							<div class="flex h-6 w-6 flex-shrink-0 items-center justify-center rounded-full bg-purple-100">
								<svg class="h-4 w-4 text-purple-600" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2.5">
									<path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
								</svg>
							</div>
							<div class="flex-1 text-base text-neutral-700 leading-relaxed">
								ללא עמלות או תשלומים נוספים
							</div>
						</div>
					</div>
				</div>
			</div>
			
			<!-- Trust badges -->
			<div class="mt-8 flex items-center justify-center gap-x-6 text-sm text-neutral-500">
				<div class="flex items-center gap-x-2">
					<svg class="h-5 w-5 text-purple-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />
					</svg>
					<span>13 שנות ניסיון</span>
				</div>
				<div class="flex items-center gap-x-2">
					<svg class="h-5 w-5 text-purple-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z" />
					</svg>
					<span>650+ תלמידים</span>
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
