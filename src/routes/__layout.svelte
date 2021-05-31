<script lang="ts">
	import '../app.postcss';
	import { base } from '$app/paths';
</script>

<svelte:head>
	<link rel="icon" type="image/png" href="{base}/favicon.png" />
	<link rel="manifest" href="{base}/manifest.json" />
</svelte:head>

<main class="h-screen">
	<slot />
</main>
