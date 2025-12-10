<script lang="ts">
	import '../app.css';
	import Navigation from '$lib/components/Navigation.svelte';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<meta charset="utf-8" />
	<meta name="viewport" content="width=device-width, initial-scale=1" />
	<meta name="description" content="TableTime - онлайн-бронирование столиков в ресторанах" />
</svelte:head>

<Navigation />

<main>
	{@render children()}
</main>

<footer class="footer">
	<div class="container">
		<p>&copy; 2025 ООО "ТейблТайм". Все права защищены.</p>
	</div>
</footer>
