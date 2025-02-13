<script lang="ts">
	import '../app.css';
	let { children } = $props();
</script>

<svelte:head>
	{#if import.meta.env.MODE === 'development'}
		<script src="https://cdn.tailwindcss.com"></script>
	{/if}
</svelte:head>

{@render children()}
