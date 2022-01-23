<script>
	import Title from '$lib/title.svelte';
	import '../../styles/global.css';
</script>

<header>
	<nav>
		<Title />
		<div class="links">
			<a href="/">Home</a>
			<a href="/about">About</a>
			<a href="/guides">Guides</a>
		</div>
	</nav>
</header>
<main>
	<slot />
</main>

<footer>
	<p>Copyright Ninja Gaming</p>
</footer>

<style>
	header {
		text-align: center;
		background-color: #0001;
	}
	main {
		max-width: 960px;
		margin: 20px auto;
	}
	footer {
		text-align: center;
	}
	.links {
		margin-left: auto;
	}
	.links a {
		margin-left: 10px;
	}
	nav {
		display: flex;
		max-width: 960px;
		margin: 0 auto;
		align-items: center;
		justify-content: center;
	}
</style>
