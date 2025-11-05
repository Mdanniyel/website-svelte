<script>
	import Hero from '$lib/sections/Hero.svelte';
	import About from '$lib/sections/About.svelte';
	import Services from '$lib/sections/Services.svelte';
</script>

<div class="h-20 bg-linear-to-br from-slate-900 to-slate-800"></div>

<Hero />

<About />

<Services />

<!-- מחירים -->
<section class="relative -mt-14 rounded-3xl bg-white px-8 py-20 shadow-lg">
	<div class="container mx-auto max-w-4xl">
		<h2 class="mb-8 text-center text-4xl font-extrabold tracking-tighter text-slate-900">
			תעריפים
		</h2>
		<div class="mb-12 rounded-2xl bg-linear-to-br from-blue-50 to-indigo-50 p-8 shadow-md">
			<p class="mb-4 text-center text-xl text-slate-700">
				שיעור פרטי: <strong class="text-2xl text-blue-600">125 ₪</strong> לשיעור של 45 דקות
			</p>
			<ul class="space-y-3 text-slate-600">
				<li class="flex items-center gap-3">
					<span class="text-blue-500">✓</span>
					<span>התשלום מתבצע בתום השיעור</span>
				</li>
				<li class="flex items-center gap-3">
					<span class="text-blue-500">✓</span>
					<span>ביטול שיעור מחייב הודעה מראש של <strong>12</strong> שעות לפחות</span>
				</li>
			</ul>
		</div>

		<h2 class="mb-6 text-center text-3xl font-bold tracking-tight text-slate-900">אזורי השירות</h2>
		<p class="mb-6 text-center text-lg text-slate-600">אני מגיע לבית התלמיד באזורים הבאים:</p>
		<div class="mb-6 grid grid-cols-2 gap-4 md:grid-cols-4">
			<div class="rounded-xl bg-slate-50 p-4 text-center shadow-sm transition hover:shadow-md">
				<span class="font-semibold text-slate-700">פתח תקווה</span>
			</div>
			<div class="rounded-xl bg-slate-50 p-4 text-center shadow-sm transition hover:shadow-md">
				<span class="font-semibold text-slate-700">רמת גן</span>
			</div>
			<div class="rounded-xl bg-slate-50 p-4 text-center shadow-sm transition hover:shadow-md">
				<span class="font-semibold text-slate-700">גבעתיים</span>
			</div>
			<div class="rounded-xl bg-slate-50 p-4 text-center shadow-sm transition hover:shadow-md">
				<span class="font-semibold text-slate-700">קריית אונו</span>
			</div>
		</div>
		<p class="text-center text-lg font-semibold text-blue-600">שיעורים מקוונים זמינים לכל הארץ 🌐</p>
	</div>
</section>

<!-- שאלות נפוצות -->
<section class="relative -mt-14 rounded-3xl bg-slate-900 px-8 py-20 text-white">
	<div class="container mx-auto max-w-3xl">
		<h2 class="mb-12 text-center text-4xl font-extrabold tracking-tighter">שאלות נפוצות</h2>

		<div class="space-y-6">
			<div class="rounded-2xl bg-slate-800/50 p-6 shadow-lg backdrop-blur-sm transition hover:bg-slate-800">
				<h3 class="mb-3 text-xl font-semibold text-blue-300">
					כמה זמן לוקח לראות שיפור בציונים?
				</h3>
				<p class="leading-relaxed text-slate-200">
					בדרך כלל תלמידים רואים שיפור ניכר כבר אחרי 3-4 שיעורים. השיפור תלוי ברמת התלמיד
					ובהשקעה שלו בבית.
				</p>
			</div>

			<div class="rounded-2xl bg-slate-800/50 p-6 shadow-lg backdrop-blur-sm transition hover:bg-slate-800">
				<h3 class="mb-3 text-xl font-semibold text-blue-300">האם אתה מספק חומרי לימוד?</h3>
				<p class="leading-relaxed text-slate-200">
					כן, אני מכין חומרי לימוד מותאמים, תרגילים נוספים וסיכומי חומר לפי הצורך של כל תלמיד.
				</p>
			</div>

			<div class="rounded-2xl bg-slate-800/50 p-6 shadow-lg backdrop-blur-sm transition hover:bg-slate-800">
				<h3 class="mb-3 text-xl font-semibold text-blue-300">
					מה קורה אם התלמיד לא מבין משהו בשיעור?
				</h3>
				<p class="leading-relaxed text-slate-200">
					אני תמיד זמין לשאלות גם בין השיעורים דרך הודעות או טלפון. החזרה על החומר היא חלק בלתי
					נפרד מהתהליך.
				</p>
			</div>

			<div class="rounded-2xl bg-slate-800/50 p-6 shadow-lg backdrop-blur-sm transition hover:bg-slate-800">
				<h3 class="mb-3 text-xl font-semibold text-blue-300">מה המלצת לגבי תדירות השיעורים?</h3>
				<p class="leading-relaxed text-slate-200">
					בדרך כלל אני ממליץ על שיעור אחד בשבוע לתלמידים רגילים, ושני שיעורים בשבוע לתלמידים
					שצריכים שיפור מהיר או לקראת בחינות.
				</p>
			</div>
		</div>
	</div>
</section>

<section class="container mx-auto max-w-3xl px-8 py-20">
	<h2 class="mb-8 text-center text-4xl font-extrabold tracking-tighter text-slate-900">
		איפה אני מלמד?
	</h2>
	<div class="rounded-2xl bg-linear-to-br from-slate-50 to-blue-50 p-8 shadow-lg">
		<p class="text-justify leading-relaxed tracking-wide text-slate-700">
			אני מלמד פרונטלית באזורים רמת גן, גבעתיים, פתח תקווה וקריית אונו, מתוך אמונה שהשיעור
			הפרונטלי הוא הדרך האפקטיבית ביותר ללמידה. בנוסף, אני מציע גם שיעורים מרוחקים דרך המחשב, כך
			שאני יכול לעזור לכם מכל מקום בארץ. עם זאת, אם באזור שלכם יש מורה פרונטלי טוב, אני ממליץ
			בחום לבחור באפשרות הזו – איכות השיעור במפגש פנים אל פנים תמיד תהיה גבוהה יותר. בין אם
			פרונטלית ובין אם מרחוק, אני כאן כדי לעזור לכם להצליח!
		</p>
	</div>
</section>
