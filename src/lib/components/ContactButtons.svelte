<script>
	import PhoneIcon from '$lib/components/icons/PhoneIcon.svelte';
	import WhatsappIcon from '$lib/components/icons/WhatsappIcon.svelte';
</script>

<nav class="mt-4 flex justify-center gap-3.5 text-center text-3xl">
	<button
		type="button"
		aria-label="Phone Number"
		class="flex w-1/2 grow justify-center rounded-lg border border-black bg-linear-to-r from-stone-900 to-stone-800 fill-white py-1.5 text-white hover:bg-linear-to-br focus:ring-4 focus:ring-blue-300 dark:focus:ring-blue-800"
	>
		<PhoneIcon />
	</button>
	<button
		type="button"
		aria-label="Whatsapp Number"
		class="flex w-1/2 grow justify-center rounded-lg border border-black py-1.5 hover:bg-linear-to-br focus:ring-4 focus:ring-green-300 dark:focus:ring-green-800"
	>
		<WhatsappIcon />
	</button>
</nav>
