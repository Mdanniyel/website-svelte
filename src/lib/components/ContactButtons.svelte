<script>
	import PhoneIcon from '$lib/components/icons/PhoneIcon.svelte';
	import WhatsappIcon from '$lib/components/icons/WhatsappIcon.svelte';
</script>

<!-- גרסה 8: Perfect White - Same Size + Gradient Border + Animations -->
<nav class="mt-8 flex justify-center gap-6 text-center">
	<!-- Phone Button - Icon Only (SAME SIZE AS WHATSAPP) -->
	<a
		href="tel:+972502727044"
		aria-label="התקשר עכשיו"
		class="floating-subtle group relative flex h-[72px] items-center justify-center overflow-hidden rounded-2xl border-2 border-gray-200 bg-white px-8 shadow-lg transition-all duration-500 hover:scale-110 hover:shadow-2xl"
	>
		<!-- Gradient border effect (from v7) -->
		<div
			class="absolute -inset-0.5 rounded-2xl bg-gradient-to-r from-blue-500 via-purple-500 to-pink-500 opacity-0 transition-opacity duration-500 group-hover:opacity-100"
		></div>

		<!-- Inner white background -->
		<div class="absolute inset-0.5 rounded-2xl bg-white"></div>

		<!-- Subtle gradient background on hover -->
		<div
			class="absolute inset-0 rounded-2xl bg-gradient-to-br from-blue-50/50 via-purple-50/50 to-pink-50/50 opacity-0 transition-opacity duration-500 group-hover:opacity-100"
		></div>

		<!-- Animated glowing shadow -->
		<div
			class="absolute -inset-2 rounded-2xl bg-gradient-to-r from-blue-500 via-purple-500 to-pink-500 opacity-0 blur-xl transition-all duration-500 group-hover:opacity-50"
		></div>

		<!-- Icon with color change and glow (SAME SIZE) -->
		<div
			class="relative z-10 text-black transition-all duration-300 group-hover:scale-110 group-hover:text-blue-600 group-hover:drop-shadow-[0_0_12px_rgba(59,130,246,0.9)]"
		>
			<PhoneIcon />
		</div>

		<!-- Shine sweep -->
		<div
			class="absolute inset-0 -translate-x-full bg-gradient-to-r from-transparent via-blue-400/30 to-transparent transition-transform duration-700 group-hover:translate-x-full"
		></div>

		<!-- Pulse ring -->
		<div
			class="pulse-ring absolute inset-0 rounded-2xl border-2 border-blue-400/50 opacity-0 group-hover:opacity-100"
		></div>
	</a>

	<!-- WhatsApp Button - Icon + Text -->
	<a
		href="https://wa.me/972502727044"
		target="_blank"
		rel="noopener noreferrer"
		aria-label="שלח הודעה בוואטסאפ"
		class="floating-subtle group relative flex h-[72px] items-center justify-center gap-3 overflow-hidden rounded-2xl border-2 border-gray-200 bg-white px-8 shadow-lg transition-all duration-500 hover:scale-110 hover:shadow-2xl"
	>
		<!-- Gradient border effect (from v7) -->
		<div
			class="absolute -inset-0.5 rounded-2xl bg-gradient-to-r from-green-400 via-emerald-500 to-teal-500 opacity-0 transition-opacity duration-500 group-hover:opacity-100"
		></div>

		<!-- Inner white background -->
		<div class="absolute inset-0.5 rounded-2xl bg-white"></div>

		<!-- Subtle gradient background on hover -->
		<div
			class="absolute inset-0 rounded-2xl bg-gradient-to-br from-green-50/50 via-emerald-50/50 to-teal-50/50 opacity-0 transition-opacity duration-500 group-hover:opacity-100"
		></div>

		<!-- Animated glowing shadow -->
		<div
			class="absolute -inset-2 rounded-2xl bg-gradient-to-r from-green-400 via-emerald-500 to-teal-500 opacity-0 blur-xl transition-all duration-500 group-hover:opacity-50"
		></div>

		<!-- Icon with color change and glow (SAME SIZE) -->
		<div
			class="relative z-10 text-black transition-all duration-300 group-hover:scale-110 group-hover:text-green-600 group-hover:drop-shadow-[0_0_12px_rgba(34,197,94,0.9)]"
		>
			<WhatsappIcon />
		</div>

		<!-- Text with color change -->
		<span
			class="relative z-10 text-lg font-semibold tracking-wide text-black transition-all duration-300 group-hover:text-green-700 group-hover:drop-shadow-[0_0_8px_rgba(34,197,94,0.7)]"
		>
			WhatsApp
		</span>

		<!-- Shine sweep -->
		<div
			class="absolute inset-0 -translate-x-full bg-gradient-to-r from-transparent via-green-400/30 to-transparent transition-transform duration-700 group-hover:translate-x-full"
		></div>

		<!-- Pulse ring -->
		<div
			class="pulse-ring absolute inset-0 rounded-2xl border-2 border-green-400/50 opacity-0 group-hover:opacity-100"
		></div>
	</a>
</nav>

<style>
	/* Subtle floating animation to attract attention */
	.floating-subtle {
		animation: float-gentle 4s ease-in-out infinite;
	}

	@keyframes float-gentle {
		0%,
		100% {
			transform: translateY(0px);
		}
		50% {
			transform: translateY(-6px);
		}
	}

	/* Pulse ring animation */
	.pulse-ring {
		animation: pulse-ring 1.5s cubic-bezier(0.4, 0, 0.6, 1) infinite;
	}

	@keyframes pulse-ring {
		0% {
			transform: scale(1);
			opacity: 0.8;
		}
		50% {
			transform: scale(1.05);
			opacity: 0.4;
		}
		100% {
			transform: scale(1.1);
			opacity: 0;
		}
	}

	/* Speed up floating on hover */
	a:hover.floating-subtle {
		animation: float-gentle 2s ease-in-out infinite;
	}
</style>
