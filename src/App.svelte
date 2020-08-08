<script>
	import Window from "./screens/Window.svelte";

	let state = 'welcome' // or 'playing';
</script>

<main>
	{#if state === 'welcome'}
		<Window />
	{:else if state === 'playing'}
		<p>playing screen goes here</p>
	{/if}
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 800px;
		margin: 0 auto;
		height: 100%;
		display: flex;
		flex-direction: column;
		justify-content: center;
	}
</style>