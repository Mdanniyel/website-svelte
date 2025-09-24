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
<section class="py-8">
	<h2 class="mb-4 text-2xl font-semibold">תעריפים</h2>
	<p class="mb-2">שיעור פרטי: <strong>125 ₪</strong> לשיעור של 45 דקות</p>
	<ul class="list-inside list-disc">
		<li>התשלום מתבצע בתום השיעור</li>
		<li>ביטול שיעור מחייב הודעה מראש של <strong>12</strong> שעות לפחות</li>
	</ul>

	<h2 class="mb-4 text-2xl font-semibold">אזורי השירות</h2>
	<p class="mb-4">אני מגיע לבית התלמיד באזורים הבאים:</p>
	<ul class="mb-4 list-inside list-disc">
		<li>פתח תקווה</li>
		<li>רמת גן</li>
		<li>גבעתיים</li>
		<li>קריית אונו</li>
	</ul>
	<p class="font-medium">שיעורים מקוונים זמינים לכל הארץ</p>
</section>

<!-- שאלות נפוצות -->
<section class="py-8">
	<h2 class="mb-4 text-2xl font-semibold">שאלות נפוצות</h2>

	<h3 class="font-medium">כמה זמן לוקח לראות שיפור בציונים?</h3>
	<p class="mb-4">
		בדרך כלל תלמידים רואים שיפור ניכר כבר אחרי 3-4 שיעורים. השיפור תלוי ברמת התלמיד ובהשקעה שלו
		בבית.
	</p>

	<h3 class="font-medium">האם אתה מספק חומרי לימוד?</h3>
	<p class="mb-4">
		כן, אני מכין חומרי לימוד מותאמים, תרגילים נוספים וסיכומי חומר לפי הצורך של כל תלמיד.
	</p>

	<h3 class="font-medium">מה קורה אם התלמיד לא מבין משהו בשיעור?</h3>
	<p class="mb-4">
		אני תמיד זמין לשאלות גם בין השיעורים דרך הודעות או טלפון. החזרה על החומר היא חלק בלתי נפרד
		מהתהליך.
	</p>

	<h3 class="font-medium">מה המלצת לגבי תדירות השיעורים?</h3>
	<p>
		בדרך כלל אני ממליץ על שיעור אחד בשבוע לתלמידים רגילים, ושני שיעורים בשבוע לתלמידים שצריכים שיפור
		מהיר או לקראת בחינות.
	</p>
</section>

<!-- צור קשר -->
<!-- <section class="py-8">
	<h2 class="mb-4 text-2xl font-semibold">צור קשר</h2>
	<p class="mb-4">בואו נתחיל את המסע להצלחה בפיזיקה! אני זמין לכל שאלה ובקשה.</p>
	<form class="max-w-md space-y-4">
		<input type="text" placeholder="שם מלא" class="w-full rounded border p-2" />
		<input type="email" placeholder="אימייל" class="w-full rounded border p-2" />
		<textarea placeholder="הודעה" class="w-full rounded border p-2"></textarea>
		<button type="submit" class="rounded bg-blue-600 px-4 py-2 text-white">שלח</button>
	</form>
</section> -->

<section class="container mx-auto max-w-lg py-20">
	<h2 class="mb-8 text-center text-4xl font-extrabold tracking-tighter">איפה אני מלמד?</h2>
	<p class="text-justify tracking-wide">
		אני מלמד פרונטלית באזורים רמת גן, גבעתיים, פתח תקווה וקריית אונו, מתוך אמונה שהשיעור הפרונטלי
		הוא הדרך האפקטיבית ביותר ללמידה. בנוסף, אני מציע גם שיעורים מרוחקים דרך המחשב, כך שאני יכול
		לעזור לכם מכל מקום בארץ. עם זאת, אם באזור שלכם יש מורה פרונטלי טוב, אני ממליץ בחום לבחור באפשרות
		הזו – איכות השיעור במפגש פנים אל פנים תמיד תהיה גבוהה יותר. בין אם פרונטלית ובין אם מרחוק, אני
		כאן כדי לעזור לכם להצליח!
	</p>
</section>
