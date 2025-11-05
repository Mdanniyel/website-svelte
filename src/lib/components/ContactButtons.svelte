<script>
	import PhoneIcon from '$lib/components/icons/PhoneIcon.svelte';
	import WhatsappIcon from '$lib/components/icons/WhatsappIcon.svelte';
</script>

<nav class="mt-8 flex justify-center gap-4 text-center text-3xl">
	<button
		type="button"
		aria-label="Phone Number"
		class="flex w-1/2 grow transform justify-center rounded-xl border-2 border-slate-300 bg-linear-to-br from-slate-900 to-slate-800 fill-white py-3 text-white shadow-lg transition-all duration-200 hover:scale-105 hover:shadow-xl focus:ring-4 focus:ring-blue-300 dark:focus:ring-blue-800"
	>
		<PhoneIcon />
	</button>
	<button
		type="button"
		aria-label="Whatsapp Number"
		class="flex w-1/2 grow transform justify-center rounded-xl border-2 border-green-500 bg-linear-to-br from-green-600 to-green-700 py-3 text-white shadow-lg transition-all duration-200 hover:scale-105 hover:shadow-xl focus:ring-4 focus:ring-green-300 dark:focus:ring-green-800"
	>
		<WhatsappIcon />
	</button>
</nav>
