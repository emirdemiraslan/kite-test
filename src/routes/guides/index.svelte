<script context="module">
	export async function load({ fetch }) {
		const res = await fetch('https://jsonplaceholder.typicode.com/posts');
		const guides = await res.json();
		if (res.ok) {
			return {
				props: {
					guides
				}
			};
		}
		return {
			status: res.status,
			error: new Error('error')
		};
	}
</script>

<script>
	export let guides;
</script>

<h1>GUIDES</h1>
<div class="guides">
	<ul>
		{#each guides as guide},
			<li>
				<a sveltekit:prefetch href={`/guides/${guide.id}`}>{guide.title}</a>
			</li>
		{/each}
	</ul>
</div>
