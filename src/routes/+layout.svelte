<script lang="ts">
	import '../app.css';
	let { children } = $props();
</script>

<svelte:head>
	{#if import.meta.env.MODE === 'development'}
		<script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
	{/if}
</svelte:head>

{@render children()}
