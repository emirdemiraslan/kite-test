<script>
	import Title from '$lib/title.svelte';
	import '../styles/global.css';
</script>

<header>
	<Title />
</header>
<main>
	<slot />
</main>

<footer>
	<p>Copyright Ninja Gaming</p>
</footer>

<style>
	header {
		display: flex;
		align-items: center;
		justify-content: center;
	}
	main {
		max-width: 960px;
		margin: 20px auto;
	}
	footer {
		text-align: center;
	}
</style>
