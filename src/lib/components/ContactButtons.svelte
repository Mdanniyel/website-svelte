<script>
	import PhoneIcon from '$lib/components/icons/PhoneIcon.svelte'
	import WhatsappIcon from '$lib/components/icons/WhatsappIcon.svelte'

	function openWhatsappChat() {
		const whatsappUrl = 'https://wa.me/972502727044';
		window.open(whatsappUrl, '_blank');
	}

	function initiatePhoneCall() {
		const phoneUrl = 'tel:+972502727044';
		window.open(phoneUrl, '_self');
	}
</script>

<nav class="mt-4 flex justify-center gap-3.5 text-center text-3xl">
	<button
		type="button"
		aria-label="Phone Number"
		class="flex w-1/2 grow justify-center rounded-lg border border-black bg-gradient-to-r from-stone-900 to-stone-800 fill-white py-1.5 text-white hover:bg-gradient-to-br"
		on:click={initiatePhoneCall}
	>
		<PhoneIcon />
	</button>
	<button
		type="button"
		aria-label="Whatsapp Number"
		class="flex w-1/2 grow justify-center rounded-lg border border-black py-1.5 hover:bg-gradient-to-br"
		on:click={openWhatsappChat}
	>
		<WhatsappIcon />
	</button>
</nav>

<style>
	button {
		position: relative;
		overflow: hidden;
		transition: transform 0.3s ease, box-shadow 0.3s ease;
	}
	button::before {
		content: '';
		position: absolute;
		top: 50%;
		left: 50%;
		width: 300%;
		height: 300%;
		background: rgba(255, 255, 255, 0.15);
		transform: translate(-50%, -50%) scale(0);
		transition: transform 0.5s ease;
		border-radius: 50%;
	}
	button:hover::before {
		transform: translate(-50%, -50%) scale(1);
	}
	button:hover {
		transform: scale(1.05);
		box-shadow: 0 8px 15px rgba(0, 0, 0, 0.3);
	}
</style>