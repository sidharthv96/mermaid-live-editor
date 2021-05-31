<script lang="ts">
	import '../app.postcss';
	import { base } from '$app/paths';
	import { onMount } from 'svelte';
	// This can be removed once https://github.com/sveltejs/kit/issues/1612 is fixed.
	// Then rename temp-service-worker to service-worker and vite will bundle it automatically.
	onMount(() => {
		if ('serviceWorker' in navigator) {
			navigator.serviceWorker.register(`${base}/temp-service-worker.js`);
		}
	});
</script>

<svelte:head>
	<link rel="icon" type="image/png" href="{base}/favicon.png" />
	<link rel="manifest" href="{base}/manifest.json" />
</svelte:head>

<main class="h-screen">
	<slot />
</main>
